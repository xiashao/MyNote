- ## Transformer bug log tip
	- navigation.session: update nav status to show nav info
	- tasdk to show vers
- [[Mar 30th, 2022]]
- 10:30
- ## TRANS-3775
- Background: could not find results for Bob and Betty Beyster Building
- Analysis for local build
	- Action: search "bob and betty"
	- Url: http://apinastg.telenav.com/entity/v4/search/json?user_id=bf9e9fce-e1ee-44ba-9509-7132c71b36ee&locale=en-US&location=42.29395800000001%2C-83.717718&query=bob+and+betty&limit=20&entry_time=2022-03-30T09%3A11
	- Request :
		- Header
			- [accept-encoding: gzip
			  connection: Keep-Alive
			  host: apinastg.telenav.com
			  user-agent: okhttp/4.8.0
			  x-tn-api_key: ed41a88d-f29d-4a50-aee2-611b22dab835
			  x-tn-api_signature: ed41a88d-f29d-4a50-aee2-611b22dab835:1648639369:6927dcba9af30bcda49282df7069f388
			  x-tn-guid: ba5d8654d36db812
			  x-tn-sdkversion: 0.0.1-feature-ONBOARDSEA-50845-feedback-poc
			  x-tn-userid: bf9e9fce-e1ee-44ba-9509-7132c71b36ee](accept-encoding: gzip
			  connection: Keep-Alive
			  host: apinastg.telenav.com
			  user-agent: okhttp/4.8.0
			  x-tn-api_key: ed41a88d-f29d-4a50-aee2-611b22dab835
			  x-tn-api_signature: ed41a88d-f29d-4a50-aee2-611b22dab835:1648642279:3e38b2e866ae2334352f4aa4f5327a8e
			  x-tn-guid: ba5d8654d36db812
			  x-tn-sdkversion: 0.0.1-feature-ONBOARDSEA-50845-feedback-poc
			  x-tn-userid: bf9e9fce-e1ee-44ba-9509-7132c71b36ee)
		- Body: Not available
	- Response:
		- Header
			- [connection: keep-alive
			  content-encoding: gzip
			  content-length: 291
			  content-type: application/json;charset=UTF-8
			  date: Wed, 30 Mar 2022 02:26:43 GMT
			  response-status-code: 200
			  vary: accept-encoding
			  x-tn-process-time: 219
			  x-tn-trace-id: ID-ec2s-autodenalinautilus-01-1647888187631-0-12284523](connection: keep-alive
			  content-encoding: gzip
			  content-length: 4364
			  content-type: application/json;charset=UTF-8
			  date: Wed, 30 Mar 2022 03:15:14 GMT
			  response-status-code: 200
			  vary: accept-encoding
			  x-tn-process-time: 515
			  x-tn-trace-id: ID-ec2s-autodenalinautilus-01-1647888187631-0-12340418)
		- Body:
			- ```
			  {
			    "status": {
			      "code": "12200",
			      "message": "SUCCESS"
			    },
			    "response_time": 507,
			    "reference_id": "9a4ce17c-0a03-4999-a469-92c4e40f4b13",
			    "metadata": {
			      "counts": [
			        {
			          "type": "place",
			          "count": 20
			        }
			      ],
			      "query_resolution": {
			        "query_tags": [
			          {
			            "what": "bob and betty"
			          }
			        ],
			        "search_position": {
			          "latitude": 42.29395,
			          "longitude": -83.71771
			        }
			      },
			      "version": "Q2xvdWQ7MC4wLjEtZmVhdHVyZS1mb3JkLWV2LWRlbW8tMTYwO05BOzIxUTM7MjAyMi0wMi0xMiAxNzowNzoyMw"
			    },
			    "has_more": true,
			    "results": [
			      {
			        "id": "P-12062503",
			        "type": "place",
			        "place": {
			          "name": "Al & Bob's Painting",
			          "phone": [
			            {
			            	... ...
			            }
			            }
			         }
			   }
			  ```
		- result: no find "bob and betty"
- Analysis for "transformer-20220318115854749.log"
	- Log
		- 1774501: 03-18 14:55:49.688 12180 12180 I [Search]:SearchResultDomainAction: searchNearBy()
		   1774502: 03-18 14:55:49.688 12180 12180 I [Search]:SearchResultDomainAction: [Search] start search: queryEntity = QueryEntity(queryType=KEYWORD, keyWord=bob and Betty , categoryIdList=[], categoryName=), evFilter = null
		   1774863: 03-18 14:55:52.040 12180 12180 I [Search]:SearchResultDomainAction: [search] search response code: SUCCESS
		   1774864: 03-18 14:55:52.043 12180 12180 I [Search]:SearchResultDomainAction: [Search] search result: [SearchEntity(id=P-12062503, displayName=Al & Bob's Painting, address=3160 Pittsview Dr, Ann Arbor MI 48108, USA, originAddress=SearchAddress(addressType=null, formattedAddress=3160 Pittsview Dr, Ann Arbor MI 48108, USA, houseNumber=3160, suite=null, street=SearchStreet(body=Pittsview Dr, type=null, formattedName=Pittsview Dr), crossStreet=SearchStreet(body=null, type=null, formattedName=null), locality=null, city=Ann Arbor, county=null, state=MI, country=USA ... ...
	- result: can not find "bob and betty " in search result.
-
-
- [[Apr 1st, 2022]]
- 09:56
- ## TRANS-3821
- Background: Visual guidance shows turn on "Unnamed Road" when entering a parking lot
- Analysis for local build:
	- Reproducible : Yes
	-