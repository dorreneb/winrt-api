---
-api-id: T:Windows.Services.Maps.MapRouteManeuver
-api-type: winrt class
---

<!-- Class syntax.
public class MapRouteManeuver : Windows.Services.Maps.IMapRouteManeuver, Windows.Services.Maps.IMapRouteManeuver2, Windows.Services.Maps.IMapRouteManeuver3
-->

# Windows.Services.Maps.MapRouteManeuver

## -description
Represents actions to be taken along the path of a route leg.

## -remarks
A collection of [MapRouteManeuver](maproutemaneuver.md) objects is returned through the [Maneuvers](maprouteleg_maneuvers.md) property of a [MapRouteLeg](maprouteleg.md) object. A collection of [MapRouteLeg](maprouteleg.md) objects is returned through the [Legs](maproute_legs.md) property of a [MapRoute](maproute.md) object. A [MapRoute](maproute.md) object is returned through the [Route](maproute.md) property of the [MapRouteFinderResult](maproutefinderresult.md) when you call the methods of the [MapRouteFinder](maproutefinder.md) class.

Your [Universal Windows app](https://msdn.microsoft.com/windows/uwp/get-started/universal-application-platform-guide) must be authenticated before it can use the [MapControl](../windows.ui.xaml.controls.maps/mapcontrol.md) and map services in the [Windows.Services.Maps](windows_services_maps.md) namespace. To authenticate your app, you must specify a maps authentication key.

See [Request a maps authentication key](https://msdn.microsoft.com/windows/uwp/maps-and-location/authentication-key).

## -examples

## -see-also
[Display  routes and directions on a map](https://msdn.microsoft.com/library/bbb4c23a-8f10-41d1-81ea-271be01aed81)
