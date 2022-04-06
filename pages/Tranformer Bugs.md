- ## Transformer bug log tip
	- navigation.session: update nav status to show nav info
	- tasdk to show versions
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
	- version:
		- appVersion      :     0.500.1002
		                          libVersion      :     0.500.1002
		                          tasdkVersion    :     1.4.18.EV-Demo.2
		                          searchVersion   :     null
		                          ttsVersion      :     0.0.14
	- NavigationEvent(legIndex=0, stepIndex=0, deviated=false, currentManeuver=ManeuverInfo(legIndex=0, stepIndex=0, turnAction=3, turnAssistAction=0, leftSideDriving=false, latitude=42.432570000000005, longitude=-83.64931, lengthMeters=1466.0, laneInfo=[LaneInfo(pattern=0, preferredPattern=0, type=0), LaneInfo(pattern=3, preferredPattern=3, type=0)], streetName=, signpostName=null, exitLabel=null, roundaboutInfo=null, stepInfo=com.telenav.sdk.drivesession.model.StepInfo@7e495e4), nextManeuver=ManeuverInfo(legIndex=0, stepIndex=1, turnAction=3, turnAssistAction=0, leftSideDriving=false, latitude=42.432480000000005, longitude=-83.65034, lengthMeters=91.0, laneInfo=null, streetName=, signpostName=null, exitLabel=null, roundaboutInfo=null, stepInfo=com.telenav.sdk.drivesession.model.StepInfo@4577a4d), distanceToTurn=1460.526123046875, traveledDistance=5.603203296661377, traveledTime=0, travelEstToStop=TravelEstimation(distanceToStop=1647.0, timeToStop=155, trafficDelay=0, arrivalToStop=2022-04-01 07:58:59), travelEstToDestination=TravelEstimation(distanceToStop=1647.0, timeToStop=155, trafficDelay=0, arrivalToStop=2022-04-01 07:58:59))
	- **Conclusion : the street name and signpostName provided by TASDK are null, this issue needs TASDK team to support.**
	-
-
- [[Apr 1st, 2022]]
- 13:55
- ## TRANS-3829
- Analysis for log:
	- > 179: 03-26 11:21:50.464 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.799026, lon: 9.182561, speed: 5.86, head: 187, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	    364: 03-26 11:21:51.466 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798969, lon: 9.182550, speed: 6.80, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	    551: 03-26 11:21:52.472 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798934, lon: 9.182544, speed: 4.01, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	    741: 03-26 11:21:53.718 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798890, lon: 9.182537, speed: 3.97, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	    922: 03-26 11:21:54.730 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798857, lon: 9.182531, speed: 3.13, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   1104: 03-26 11:21:55.975 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798826, lon: 9.182526, speed: 0.90, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   1290: 03-26 11:21:57.230 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798818, lon: 9.182525, speed: 0.94, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   1468: 03-26 11:21:58.468 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798816, lon: 9.182524, speed: 0.31, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   1644: 03-26 11:21:59.472 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798816, lon: 9.182524, speed: 0.31, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   1822: 03-26 11:22:00.482 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798817, lon: 9.182525, speed: 0.23, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   2003: 03-26 11:22:01.720 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798817, lon: 9.182525, speed: 0.23, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   2181: 03-26 11:22:02.727 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798817, lon: 9.182525, speed: 0.23, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   2366: 03-26 11:22:03.972 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798817, lon: 9.182525, speed: 0.23, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   2541: 03-26 11:22:04.988 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798803, lon: 9.182522, speed: 0.62, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   2714: 03-26 11:22:05.986 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798783, lon: 9.182519, speed: 3.44, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   2902: 03-26 11:22:07.226 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798743, lon: 9.182512, speed: 4.10, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   3083: 03-26 11:22:08.234 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798697, lon: 9.182505, speed: 4.75, head: 185, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   3416: 03-26 11:22:09.482 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798634, lon: 9.182495, speed: 5.60, head: 185, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   3447: 03-26 11:22:10.486 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798565, lon: 9.182485, speed: 7.33, head: 185, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   3632: 03-26 11:22:11.741 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798497, lon: 9.182475, speed: 6.49, head: 185, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   3819: 03-26 11:22:12.990 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798332, lon: 9.182450, speed: 8.68, head: 185, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   4014: 03-26 11:22:14.001 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798270, lon: 9.182440, speed: 8.00, head: 185, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   4189: 03-26 11:22:15.249 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798185, lon: 9.182434, speed: 8.27, head: 182, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   4370: 03-26 11:22:16.487 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798113, lon: 9.182428, speed: 8.37, head: 184, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   4545: 03-26 11:22:17.512 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.798005, lon: 9.182415, speed: 8.96, head: 184, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   4724: 03-26 11:22:18.748 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.797918, lon: 9.182407, speed: 8.78, head: 182, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   4900: 03-26 11:22:20.029 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.797763, lon: 9.182403, speed: 9.40, head: 176, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   5089: 03-26 11:22:21.244 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.797680, lon: 9.182411, speed: 9.04, head: 176, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   5265: 03-26 11:22:22.493 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.797605, lon: 9.182417, speed: 9.82, head: 176, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   5455: 03-26 11:22:23.744 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.797525, lon: 9.182425, speed: 9.33, head: 175, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   5640: 03-26 11:22:24.755 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.797436, lon: 9.182434, speed: 10.52, head: 176, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   5814: 03-26 11:22:25.999 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.797256, lon: 9.182440, speed: 9.96, head: 180, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   5986: 03-26 11:22:26.999 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.797175, lon: 9.182438, speed: 9.07, head: 182, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   6158: 03-26 11:22:28.007 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.797089, lon: 9.182432, speed: 9.66, head: 182, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   6334: 03-26 11:22:29.247 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.796989, lon: 9.182423, speed: 10.83, head: 184, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   6513: 03-26 11:22:30.253 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.796905, lon: 9.182414, speed: 9.75, head: 184, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
	   6698: 03-26 11:22:31.496 15144  3697 I navigation.session: { vehicle: { status: on-route, lat: 48.796831, lon: 9.182404, speed: 9.56, head: 186, tz: { cc: DEU, name: UTC+01:00, UTC: 3600, DST: 0 }, cc: DEU } }
- Reference : https://spaces.telenav.com:8443/pages/viewpage.action?pageId=201501490
- Refer to this wiki
	- > For the above camera transitions, if a vehicle speeds up and exceeds the upper limit of the current speed limit range by at least 10mph for at least 5 seconds, then animate smoothly to the higher zoom level with an animation duration of 2 seconds. If the vehicle slows back down to the speed limit range of its current street for at least 5 seconds, then animate smoothly back to the default zoom level for the current street with an animation duration of 2 seconds. These buffers prevent the camera from transitioning immediately back and forth between ranges when driving at/near the thresholds.
- Conclusion : auto zoom is triggered only when the speed changes between different speed limits. By analyzing the log, the speed is still not more than speed limit, therefore, it will not trigger auto zoom. Could you please check if there is any related requirement that triggering auto zoom when reducing speed?
-
- [[Apr 1st, 2022]]
- 16:04
- ## TRANS-3780
- Analysis :
	- Reproducible : yes
	- When arrived, the system will search parking nearby.
	- Analysis for request and response:
		- Request Head:
			- accept-encoding: gzip
			  connection: Keep-Alive
			  host: apinastg.telenav.com
			  user-agent: okhttp/4.8.0
			  x-tn-api_key: ed41a88d-f29d-4a50-aee2-611b22dab835
			  x-tn-api_signature: ed41a88d-f29d-4a50-aee2-611b22dab835:1648832661:2a5e9f113294594bba348bf37cbd668a
			  x-tn-guid: ba5d8654d36db812
			  x-tn-sdkversion: 0.0.1-feature-ONBOARDSEA-50845-feedback-poc
			  x-tn-userid: bf9e9fce-e1ee-44ba-9509-7132c71b36ee
		- Url: http://apinastg.telenav.com/entity/v4/search/json?user_id=bf9e9fce-e1ee-44ba-9509-7132c71b36ee&locale=en-US&location=42.43165%2C-83.76949&f.cat.list=600&limit=3&entry_time=2022-04-01T14%3A04
		- Response
			- Head
				- connection: keep-alive
				  content-encoding: gzip
				  content-length: 2213
				  content-type: application/json;charset=UTF-8
				  date: Fri, 01 Apr 2022 08:08:15 GMT
				  response-status-code: 200
				  vary: accept-encoding
				  x-tn-process-time: 575
				  x-tn-trace-id: ID-ec2s-autodenalinautilus-01-1647888187631-0-14695485
				- Body
					- ```
					  {
					    "status": {
					      "code": "12200",
					      "message": "SUCCESS"
					    },
					    "response_time": 563,
					    "reference_id": "a5267213-2c0a-445b-aa0c-736720f0d4d2",
					    "metadata": {
					      "counts": [
					        {
					          "type": "place",
					          "count": 3
					        }
					      ],
					      "query_resolution": {
					        "query_tags": [
					          {
					            "filters": [
					              {
					                "type": "category",
					  	... ...	
					  }
					  ```
			- Conclusion: We cant search a parking nearby, one possibility is that Here data miss a parking in this location, therefore I need the search team to help investigate this issue.
-
- [[Apr 2nd, 2022]]
- 10:32
- ## TRANS-3772
	- Background: System not showing next manervour
	- Analysis for Log
		- > 1503538: 03-18 14:32:01.184 12180 21240 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1503672: 03-18 14:32:02.424 12180 20718 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1503943: 03-18 14:32:03.694 12180 21075 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1504126: 03-18 14:32:04.931 12180 21240 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1504282: 03-18 14:32:05.930 12180 17882 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1504568: 03-18 14:32:06.940 12180 21237 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1504804: 03-18 14:32:07.936 12180 20718 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1505082: 03-18 14:32:09.187 12180 21179 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1505638: 03-18 14:32:11.428 12180 20646 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1505814: 03-18 14:32:12.179 12180 21240 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1506809: 03-18 14:32:13.426 12180 20718 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1507523: 03-18 14:32:14.683 12180 21076 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1507803: 03-18 14:32:15.925 12180 20487 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1508021: 03-18 14:32:16.927 12180 21179 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1508289: 03-18 14:32:18.172 12180 21176 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1508546: 03-18 14:32:19.423 12180 21181 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1508780: 03-18 14:32:20.671 12180 21179 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1509017: 03-18 14:32:21.677 12180 21179 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1509230: 03-18 14:32:22.926 12180 20719 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1509557: 03-18 14:32:24.174 12180 21179 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1509775: 03-18 14:32:25.175 12180 20487 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1510091: 03-18 14:32:26.181 12180 20487 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1510309: 03-18 14:32:27.196 12180 21177 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1510530: 03-18 14:32:28.432 12180 20487 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1510813: 03-18 14:32:29.682 12180 21076 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1511012: 03-18 14:32:30.935 12180 21076 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1511283: 03-18 14:32:32.187 12180 21181 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1511524: 03-18 14:32:33.431 12180 21238 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1511743: 03-18 14:32:34.433 12180 21237 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1512062: 03-18 14:32:35.680 12180 21278 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1512179: 03-18 14:32:36.181 12180 21178 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1512531: 03-18 14:32:37.187 12180 21243 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1512778: 03-18 14:32:38.191 12180 21076 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1513071: 03-18 14:32:39.436 12180 21177 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1513312: 03-18 14:32:40.689 12180 17882 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1513544: 03-18 14:32:41.931 12180 20718 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1513755: 03-18 14:32:42.938 12180 20719 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1513961: 03-18 14:32:43.937 12180 21232 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1514225: 03-18 14:32:45.193 12180 20718 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1514441: 03-18 14:32:46.196 12180 21278 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1514685: 03-18 14:32:47.448 12180 21239 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1514923: 03-18 14:32:48.690 12180 21410 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1515141: 03-18 14:32:49.694 12180 21179 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1515365: 03-18 14:32:50.695 12180 21177 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1515615: 03-18 14:32:51.950 12180 21243 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1515820: 03-18 14:32:52.948 12180 20718 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1516078: 03-18 14:32:54.196 12180 21179 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		   1516241: 03-18 14:32:55.200 12180 21238 D [MovingMap]:MovingMapDomainAction: updateTightTurnIcon >> hasTightTurn? false, approached ? true
		- The attribute "hasTightTurn" always is false at 2:32 pm.
		- Refer to codes, only when hasTightTurn and approached are true, navigation panel will show the tight turn info.
		- Conclusion: From the code logic, the display of the next maneuver needs to meet some conditions instead of being displayed at any time. So, could you please share your opinion about it?
-
-
- [[Apr 6th, 2022]]
- 11:26
- ## TRANS-3769
- Background: Search- two entries for Hill Auditorium in search results
- Reproducible: Yes
- Analysis for Log
	- > 03-18 14:30:07.419 12180 12180 I [Search]:OneBoxDomainAction: [AutoComplete] auto complete result: AutoCompleteResponse(code=SUCCESS, message=SUCCESS, responseTime=63, responseType=CLOUD, results=[AutoCompleteSuggestion(entity=SearchEntity(id=P-2264101, **displayName=Hill Auditorium, address=825 N University Ave, Ann Arbor (Burns Park) MI 48109**, USA, originAddress=SearchAddress(addressType=null, formattedAddress=825 N University Ave, Ann Arbor (Burns Park) MI 48109, USA, houseNumber=825, suite=null, street=SearchStreet(body=N University Ave, type=null, formattedName=N University Ave), crossStreet=SearchStreet(body=null, type=null, formattedName=null), locality=null, city=Ann Arbor, county=null, state=MI, country=USA, postalCode=48109, neighbourhood=null, addressLines=[]), label=Hill Auditorium, distance=1475.0, categoryName=Performing arts, categoryId=195, geoCoordinates=LatLon(lat=42.27878, lon=-83.73922), navCoordinates=LatLon(lat=42.27866, lon=-83.73922), rating=0.0, ratingCount=0, facets=null, phoneNumbers=[7347648350], isAddedCharger=false, isEVStation=false, hasEVCharger=false, orderAhead=false, searchStoreStatusOption=TRADE_OPEN, commerceLocationId=, type=PLACE, evParameter=null, brands=[], promotionCoupon=null), label=Hill Auditorium, 825 N University Ave, Ann Arbor (Burns Park) MI 48109, USA, type=ENTITY, category=null), AutoCompleteSuggestion(entity=SearchEntity(id=P-YP-BfRPxsz2EUxhmLnXXg30jQ, **displayName=Hill Auditorium, address=825 North University, Ann Arbor MI 48109**, USA, originAddress=SearchAddress(addressType=null, formattedAddress=825 North University, Ann Arbor MI 48109, USA, houseNumber=825, suite=null, street=SearchStreet(body=North University, type=null, formattedName=North University), crossStreet=SearchStreet(body=null, type=null, formattedName=null), locality=null, city=Ann Arbor, county=null, state=MI, country=USA, postalCode=48109, neighbourhood=null... ...
	- There are two searchEntity with same name "Hill Auditorium"
	-
- Analysis for local build
	- URL: http://apinastg.telenav.com/entity/v4/suggestion/json?user_id=bf9e9fce-e1ee-44ba-9509-7132c71b36ee&locale=en-US&query=hill+audi&location=42.26795087939869%2C-83.74715119600296&include.entity=true
	- Request
		- accept-encoding: gzip
		  connection: Keep-Alive
		  host: apinastg.telenav.com
		  user-agent: okhttp/4.8.0
		  x-tn-api_key: ed41a88d-f29d-4a50-aee2-611b22dab835
		  x-tn-api_signature: ed41a88d-f29d-4a50-aee2-611b22dab835:1649254055:d061df8f10bb2a28d6c28ba9cb722b0c
		  x-tn-guid: ba5d8654d36db812
		  x-tn-sdkversion: 0.0.1-feature-ONBOARDSEA-50845-feedback-poc
		  x-tn-userid: bf9e9fce-e1ee-44ba-9509-7132c71b36ee
	- Response
		- connection: keep-alive
		  content-encoding: gzip
		  content-length: 1385
		  content-type: application/json;charset=UTF-8
		  date: Wed, 06 Apr 2022 05:12:57 GMT
		  response-status-code: 200
		  vary: accept-encoding
		  x-tn-process-time: 104
		  x-tn-trace-id: ID-ec2s-autodenalinautilus-01-1647888187631-0-18151864
		- Body
			- ```
			  {
			    "status": {
			      "code": "12200",
			      "message": "SUCCESS"
			    },
			    "reference_id": "fcd1a837-0f5c-443f-9784-185764617e7a",
			    "response_time": 96,
			    "metadata": {
			      "version": "Q2xvdWQ7MC4wLjEtZmVhdHVyZS1mb3JkLWV2LWRlbW8tMTYwO05BOzIxUTM7MjAyMi0wMi0xMiAxNzowNzoyMw"
			    },
			    "results": [
			      {
			        "id": "P-2264101",
			        "type": "entity",
			        "label": "Hill Auditorium, 825 N University Ave, Ann Arbor (Burns Park) MI 48109, USA",
			        }
			  ...
			   {
			        "id": "P-YP-BfRPxsz2EUxhmLnXXg30jQ",
			        "type": "entity",
			        "label": "Hill Auditorium, 825 North University, Ann Arbor MI 48109, USA",
			        "query": "ENTITY_ID=P-YP-BfRPxsz2EUxhmLnXXg30jQ;sid=a4cc4c0e-9ad4-4290-9000-4594a9485a6e;position=1;originalQuery=hill audi;source=autosuggest;",
			  ...
			  }
			  ```
- Conclusion: There are two search entities with the same name "Hill Auditorium", and they have the similar address. So I need Search team support to check if it is normal or not.