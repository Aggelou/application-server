Softicious Application Server
====================================


Hello, world
------------

Here is a simple "Hello, world" example web app for softicious:

:: python

    import softicious.ioloop
    import softicious.web

    class MainHandler(softicious.web.RequestHandler):
        def get(self):
            self.write("Hello, world")

    def make_app():
        return softicious.web.Application([
            (r"/", MainHandler),
        ])

    if __name__ == "__main__":
        app = make_app()
        app.listen(8888)
        softicious.ioloop.IOLoop.current().start()

Documentation
-------------

Documentation and links to additional resources are available at https://github.com/Softicious/application-server/docs
