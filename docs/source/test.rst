Welcome to Lumache's documentation!
===================================

.. codeblock:: python

   from integration.ctix import CTIX

   ctix = CTIX("http://localhost:8000", "", "")
   api_key = 'ce2b981779dcc63d63b5818116c539c52572c8ef010403891e09b858e46daa4a'
   secret_key = '55104acaa56df66161a6e90d791534263721d19c2f2c59d7d41a9fbf0bb0229e'

   mandiant = ctix.integration.get_app(title="Virus Total")
   # acc = mandiant.add_account("jack", api_key)
   # acc = mandiant.get_account(name="jack").delete()
   # mandiant.get_account(name="john").enable()
   mandiant.get_account(name="jack").enable_action("hash")
   mandiant.enrich(127.0.0.1, "ip")
