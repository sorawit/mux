mux
===
gorilla/mux is a powerful URL router and dispatcher.

This fork adds Router.Wrap(wrapers ...func(http.Handler) http.Handler) and Route.Wrap(wrappers ...func(http.Handler) http.Handler) so that it supports middlewares.

API
---
Router.Wrap(wrappers ...func(http.Handler) http.Handler): Wraps the handlers of all routes in this router (or subrouter). This function returns back the given Router (different from other methods that mostly return new Route)

Route.Wrap(wrappers ...func(http.Handler) http.Handler): Wraps the handler of this route to the corresponding wrappers. This function can be called before or after the handler is set. This function returns back the given Route

Read the full documentation here: http://www.gorillatoolkit.org/pkg/mux
