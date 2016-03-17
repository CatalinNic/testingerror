IntegrityError at /register/
(1062, "Duplicate entry '170860' for key 'upgraded_from_id'")
Request Method:	POST
Request URL:	http://stage-ipbe.reincubate.com/register/
Django Version:	1.8.3
Exception Type:	IntegrityError
Exception Value:	
(1062, "Duplicate entry '170860' for key 'upgraded_from_id'")
Exception Location:	/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/MySQLdb/connections.py in defaulterrorhandler, line 36
Python Executable:	/usr/local/bin/uwsgi
Python Version:	2.7.3
Python Path:	
['/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/pip-1.2.1-py2.7.egg',
 '/var/www-hosts/ipbe-site/',
 '/var/www-hosts/ipbe-site/',
 '.',
 '',
 '/usr/lib/python2.7',
 '/usr/lib/python2.7/plat-linux2',
 '/usr/lib/python2.7/lib-tk',
 '/usr/lib/python2.7/lib-old',
 '/usr/lib/python2.7/lib-dynload',
 '/usr/local/lib/python2.7/dist-packages',
 '/usr/lib/python2.7/dist-packages',
 '/usr/lib/pymodules/python2.7',
 '/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages',
 '/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/newrelic-2.60.0.46',
 '/var/www-hosts/ipbe-site/restricted/virtualenv/lib/site-packages',
 '/var/www-hosts/ipbe-site/project',
 '/var/www-hosts/ipbe-site/apps']
Server time:	Thu, 17 Mar 2016 10:20:31 +0000
Traceback Switch to copy-and-paste view

/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/core/handlers/base.py in get_response
                                response = wrapped_callback(request, *callback_args, **callback_kwargs) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/newrelic-2.60.0.46/newrelic/hooks/framework_django.py in wrapper
                            return wrapped(*args, **kwargs) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/reincubate_core/billing/decorators.py in wrapper
                            return function(*args, **kwargs) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/reincubate_core/cms/decorators.py in wrap
                        return function(*args, **kwargs) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/reincubate_core/billing/views.py in payment_page
                            response = invoice.gateway_purchase(gateway_name=gateway, gateway_options=gateway_options, cc_options=cc_options) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/reincubate_core/billing/models/invoice.py in gateway_purchase
                                            options=gateway_options ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/jpmc/gateways/jpmc_gateway.py in purchase
                    return self._perform_request(request=request) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/jpmc/gateways/jpmc_gateway.py in _perform_request
                    signal.send(sender=Transaction, instance=transaction, type='purchase', reponse=response) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/dispatch/dispatcher.py in send
                        response = receiver(signal=self, sender=sender, **named) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/reincubate_core/billing/models/__init__.py in jpmc_transaction_successful
                    invoice.transaction_completed(transaction=instance, gateway='jpmc') ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/reincubate_core/billing/models/invoice.py in transaction_completed
                    Registration.create_entitlement(sender=Invoice, instance=self) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/reincubate_core/billing/models/registration.py in create_entitlement
                                        invoice_product=invoice_product ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/models/manager.py in manager_method
                            return getattr(self.get_queryset(), name)(*args, **kwargs) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/models/query.py in create
                    obj.save(force_insert=True, using=self.db) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/models/base.py in save
                                   force_update=force_update, update_fields=update_fields) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/models/base.py in save_base
                        updated = self._save_table(raw, cls, force_insert, force_update, using, update_fields) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/models/base.py in _save_table
                        result = self._do_insert(cls._base_manager, using, fields, update_pk, raw) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/models/base.py in _do_insert
                                           using=using, raw=raw) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/models/manager.py in manager_method
                            return getattr(self.get_queryset(), name)(*args, **kwargs) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/models/query.py in _insert
                    return query.get_compiler(using=using).execute_sql(return_id) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/models/sql/compiler.py in execute_sql
                            cursor.execute(sql, params) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/backends/utils.py in execute
                        return super(CursorDebugWrapper, self).execute(sql, params) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/backends/utils.py in execute
                            return self.cursor.execute(sql, params) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/utils.py in __exit__
                            six.reraise(dj_exc_type, dj_exc_value, traceback) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/backends/utils.py in execute
                            return self.cursor.execute(sql, params) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/django/db/backends/mysql/base.py in execute
                        return self.cursor.execute(query, args) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/newrelic-2.60.0.46/newrelic/hooks/database_dbapi2.py in execute
                                    *args, **kwargs) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/MySQLdb/cursors.py in execute
                        self.errorhandler(self, exc, value) ...
▶ Local vars
/var/www-hosts/ipbe-site/restricted/virtualenv/lib/python2.7/site-packages/MySQLdb/connections.py in defaulterrorhandler
                raise errorclass, errorvalue ...
▶ Local vars
Request information

GET
No GET data
POST
Variable	Value
delivery_zip	
u''
last_name	
u'test'
house	
u'test'
delivery_country	
u'GB'
products-MAX_NUM_FORMS	
u''
currency	
u'EUR'
vat_id	
u''
delivery_option	
u'1'
products-0-product_unique_identifier	
u''
acct	
u'4112 3441 1234 4113'
delivery_city	
u''
city	
u'test'
first_name	
u'test'
zip	
u'00000'
products-3-product	
u'10008'
delivery_last_name	
u''
state	
u'test'
products-4-quantity	
u'1'
company_name	
u''
cvv2	
u'999'
csrfmiddlewaretoken	
u'7E3dF4wA4X9n8ITr6aQJzt7U7Amfk5oY'
delivery_phone	
u''
products-2-quantity	
u'0'
products-0-quantity	
u'0'
products-1-product_unique_identifier	
u''
products-INITIAL_FORMS	
u'0'
delivery_first_name	
u''
products-1-product	
u'10006'
method	
u'WPP'
products-TOTAL_FORMS	
u'5'
delivery_street	
u''
products-1-quantity	
u'0'
voucher_code	
u''
products-2-product_unique_identifier	
u''
products-3-product_unique_identifier	
u''
language	
u'en'
products-4-product	
u'10014'
products-2-product	
u'10007'
products-0-product	
u'1001'
email	
u'catalin+test2@reincubate.com'
expiry_0	
u'6'
expiry_1	
u'2016'
country	
u'GB'
products-3-quantity	
u'0'
delivery_state	
u''
products-4-product_unique_identifier	
u'227841'
FILES
No FILES data
COOKIES
Variable	Value
clicky_olark	
'2085-100-10-9329%2CuLEshstndnmyrWA69W91ADA3JNQ40EKb%2CL1Pih1hkVrHV6b8W9W91AVA3JNQL0E4r'
heatmaps_g2g_134965	
'yes'
__insp_targlpu	
'http%3A%2F%2Fstage-ipbe.reincubate.com%2Fregister%2F'
__insp_targlpt	
'Purchase%20the%20iPhone%20Backup%20Extractor%20-%20open%20iTunes%20backup%20files'
_vwo_uuid_v2	
'8C7F20482C0EADB7A8E928EBCF375ED0|4350f15b3a2cd3a6e9deaebe8113f3a9'
olfsk	
'olfsk8132325022015721'
_oklv	
'1458210001029%2CL1Pih1hkVrHV6b8W9W91AVA3JNQL0E4r'
repackage_test	
'a8a15bca2cb14be0ba710f778aced8a7'
_eventqueue	
'%7B%22heatmap%22%3A%5B%5D%2C%22events%22%3A%5B%5D%7D'
_first_pageview	
'1'
_utm_og	
'%26utm_source%3Dapp%26utm_campaign%3D6.0.7.914%26utm_content%3DNagScreen_Nags-Variation-4_buygeneric%26utm_medium%3DPREVIEWS-ENABLED-extract-appointment-main-links'
_ga	
'GA1.2.1481708590.1455024325'
_okdetect	
'%7B%22token%22%3A%2214582099044020%22%2C%22proto%22%3A%22http%3A%22%2C%22host%22%3A%22stage-ipbe.reincubate.com%22%7D'
__insp_norec_sess	
'true'
__insp_nv	
'true'
_referrer_og	
'https%3A%2F%2Fwww.google.ro%2F'
__utmz	
'235397315.1456910927.15.2.utmcsr=app|utmccn=6.0.7.914|utmcmd=PREVIEWS-ENABLED-extract-appointment-main-links|utmcct=NagScreen_Nags-Variation-4_buygeneric'
_jsuid	
'4287411044'
hblid	
'uLEshstndnmyrWA69W91ADA3JNQ40EKb'
__utmt	
'1'
__insp_wid	
'1014680378'
__utmv	
'235397315.|2=Stage=post_test=1'
_okbk	
'cd4%3Dtrue%2Cvi5%3D0%2Cvi4%3D1458209904604%2Cvi3%3Dactive%2Cvi2%3Dfalse%2Cvi1%3Dfalse%2Ccd8%3Dchat%2Ccd6%3D0%2Ccd5%3Daway%2Ccd3%3Dfalse%2Ccd2%3D0%2Ccd1%3D0%2C'
sessionid	
'y1tgs60ajjpr0xcs74r4y56muq87shf7'
dwf_repackage_test	
'True'
csrftoken	
'7E3dF4wA4X9n8ITr6aQJzt7U7Amfk5oY'
__utma	
'235397315.1481708590.1455024325.1458145284.1458209904.17'
__utmb	
'235397315.12.10.1458209904'
__utmc	
'235397315'
__insp_ref	
'd'
lang	
'en'
__insp_slim	
'1458210001077'
VARIATION	
'1'
wcsid	
'L1Pih1hkVrHV6b8W9W91AVA3JNQL0E4r'
cb-enabled	
'accepted'
_ok	
'2085-100-10-9329'
META
Variable	Value
wsgi.multiprocess	
True
HTTP_REFERER	
'http://stage-ipbe.reincubate.com/register/'
uwsgi.version	
'2.0'
SCRIPT_NAME	
u''
REQUEST_METHOD	
'POST'
PATH_INFO	
u'/register/'
HTTP_ORIGIN	
'http://stage-ipbe.reincubate.com'
SERVER_PROTOCOL	
'HTTP/1.1'
QUERY_STRING	
''
UWSGI_SCHEME	
'http'
CONTENT_LENGTH	
'965'
HTTP_USER_AGENT	
'Mozilla/5.0 (Windows NT 6.1; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/49.0.2623.87 Safari/537.36'
HTTP_CONNECTION	
'close'
HTTP_COOKIE	
'_jsuid=4287411044; repackage_test=a8a15bca2cb14be0ba710f778aced8a7; _utm_og=%26utm_source%3Dapp%26utm_campaign%3D6.0.7.914%26utm_content%3DNagScreen_Nags-Variation-4_buygeneric%26utm_medium%3DPREVIEWS-ENABLED-extract-appointment-main-links; dwf_repackage_test=True; _referrer_og=https%3A%2F%2Fwww.google.ro%2F; _ga=GA1.2.1481708590.1455024325; lang=en; sessionid=y1tgs60ajjpr0xcs74r4y56muq87shf7; VARIATION=1; __utmt=1; _first_pageview=1; __insp_wid=1014680378; __insp_nv=true; __insp_ref=d; __insp_targlpu=http%3A%2F%2Fstage-ipbe.reincubate.com%2Fregister%2F; __insp_targlpt=Purchase%20the%20iPhone%20Backup%20Extractor%20-%20open%20iTunes%20backup%20files; clicky_olark=2085-100-10-9329%2CuLEshstndnmyrWA69W91ADA3JNQ40EKb%2CL1Pih1hkVrHV6b8W9W91AVA3JNQL0E4r; _okdetect=%7B%22token%22%3A%2214582099044020%22%2C%22proto%22%3A%22http%3A%22%2C%22host%22%3A%22stage-ipbe.reincubate.com%22%7D; heatmaps_g2g_134965=yes; _okbk=cd4%3Dtrue%2Cvi5%3D0%2Cvi4%3D1458209904604%2Cvi3%3Dactive%2Cvi2%3Dfalse%2Cvi1%3Dfalse%2Ccd8%3Dchat%2Ccd6%3D0%2Ccd5%3Daway%2Ccd3%3Dfalse%2Ccd2%3D0%2Ccd1%3D0%2C; _ok=2085-100-10-9329; __insp_norec_sess=true; csrftoken=7E3dF4wA4X9n8ITr6aQJzt7U7Amfk5oY; _vwo_uuid_v2=8C7F20482C0EADB7A8E928EBCF375ED0|4350f15b3a2cd3a6e9deaebe8113f3a9; _oklv=1458210001029%2CL1Pih1hkVrHV6b8W9W91AVA3JNQL0E4r; __insp_slim=1458210001077; olfsk=olfsk8132325022015721; wcsid=L1Pih1hkVrHV6b8W9W91AVA3JNQL0E4r; hblid=uLEshstndnmyrWA69W91ADA3JNQ40EKb; __utma=235397315.1481708590.1455024325.1458145284.1458209904.17; __utmb=235397315.12.10.1458209904; __utmc=235397315; __utmz=235397315.1456910927.15.2.utmcsr=app|utmccn=6.0.7.914|utmcmd=PREVIEWS-ENABLED-extract-appointment-main-links|utmcct=NagScreen_Nags-Variation-4_buygeneric; __utmv=235397315.|2=Stage=post_test=1; cb-enabled=accepted; _eventqueue=%7B%22heatmap%22%3A%5B%5D%2C%22events%22%3A%5B%5D%7D'
SERVER_NAME	
'dev.iphonebackupextractor.com'
REMOTE_ADDR	
'109.74.201.203'
wsgi.url_scheme	
'http'
SERVER_PORT	
'8081'
uwsgi.node	
'nj-web-2'
DOCUMENT_ROOT	
'/var/www-hosts/ipbe-site/docroot_collected'
HTTP_CONTENT_LENGTH	
'965'
wsgi.input	
<newrelic.api.web_transaction._WSGIInputWrapper object at 0x4acb550>
HTTP_HOST	
'stage-ipbe.reincubate.com'
wsgi.multithread	
False
HTTP_UPGRADE_INSECURE_REQUESTS	
'1'
HTTP_CACHE_CONTROL	
'max-age=0'
HTTP_CONTENT_TYPE	
'application/x-www-form-urlencoded'
REQUEST_URI	
'/register/'
HTTP_ACCEPT	
'text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8'
wsgi.version	
(1, 0)
HTTP_X_FORWARDED_FOR	
'109.74.201.203'
wsgi.errors	
<open file 'wsgi_errors', mode 'w' at 0x407e1e0>
REMOTE_PORT	
'50841'
HTTP_ACCEPT_LANGUAGE	
'en-US,en;q=0.8'
wsgi.run_once	
False
CONTENT_TYPE	
'application/x-www-form-urlencoded'
wsgi.file_wrapper	
''
CSRF_COOKIE	
u'7E3dF4wA4X9n8ITr6aQJzt7U7Amfk5oY'
HTTP_ACCEPT_ENCODING	
'gzip, deflate'
Settings
Using settings module settings
Setting	Value
LOCAL_SETTINGS	
True
BILLING_EMAIL_RECEIPT_UTM_CAMPAIGN	
'txreceipt'
PAYPAL_TEST	
True
BILLING_MOBILE_PAYMENT_TEMPLATE	
'billing/basket_checkout.mobile.html'
BILLING_EMAIL_PDF_INVOICE	
True
KILL_UNACTIVATED	
False
APP_PAYPAL_CUSTOM	
'ipbe 1x redesign'
USE_THOUSAND_SEPARATOR	
False
CSRF_COOKIE_SECURE	
False
PAYPAL_WPP_USER	
'aidan_api1.reincubate.com'
AB_TEST_NEW_FILTER	
[10010, 10011, 10012, 10013, 10014, 10019]
LANGUAGE_CODE	
'en-us'
ROOT_URLCONF	
'urls'
MANAGERS	
(('Sysadmin', 'sysadmin@reincubate.com'),)
EMAIL_HEADER	
'res/billing/email/ipbe_logo.png'
FILE_UPLOAD_DIRECTORY_PERMISSIONS	
None
BASE_DIR	
'/var/www-hosts/ipbe-site/project/..'
JPMC_AUTO_RETRY	
True
DEFAULT_CHARSET	
'utf-8'
APP_DOMAIN	
'iphonebackupextractor.com'
AWS_S3_CUSTOM_DOMAIN	
's.iphonebackupextractor.com'
STATIC_ROOT	
'../../../var/www-hosts/ipbe-site/docroot_collected'
JPMC_ORBITAL_PASSWORD	
u'********************'
BLOG_SUBTITLE	
'Free and easy to use tool for extracting iPhone, iPad and iPod Touch backup data'
AB_TEST_OLD_FILTER	
[1003, 1004, 1005]
CKEDITOR_UPLOAD_PATH	
'uploads/'
TWITTER_URL	
'http://twitter.com/reincubate'
JPMC_TIMEOUT	
90
LANGUAGE_CODE_ALIASES	
{'de': {'name': 'German', 'name_local': u'Deutsch', 'real_code': 'de'},
 'en': {'name': 'English', 'name_local': u'English', 'real_code': 'en'},
 'es': {'name': 'Spanish', 'name_local': u'Espa\xf1ol', 'real_code': 'es'},
 'fr': {'name': 'French', 'name_local': u'Fran\xe7ais', 'real_code': 'fr'},
 'jp': {'hreflang_code': 'ja',
        'name': 'Japanese',
        'name_local': u'\u65e5\u672c\u306e',
        'real_code': 'ja'},
 'zh': {'name': 'Simplified Chinese',
        'name_local': u'\u4e2d\u56fd\u7684',
        'real_code': 'zh-cn'}}
AB_TEST_COOKIE_VALUE	
'5f8ba64ede759a87fa0b913d5c0f613f'
BILLING_EMAIL_PENDING_UTM_CAMPAIGN	
'txpending'
ALLOWED_HOSTS	
['.iphonebackupextractor.com', 'www.iphonebackupextractor.com.']
MESSAGE_STORAGE	
'django.contrib.messages.storage.fallback.FallbackStorage'
APP_LATEST_VERSION	
'3.2.2'
EMAIL_SUBJECT_PREFIX	
'[Django] '
SERVER_EMAIL	
'www.iphonebackupextractor.com <noreply@www.iphonebackupextractor.com>'
SECURE_HSTS_SECONDS	
0
D	
<class 'decimal.Decimal'>
STATICFILES_FINDERS	
('reincubate_core.cms.finders.AppDirectoriesResFinder',
 'reincubate_core.cms.finders.ResFileSystemFinder')
APP_COMMISSION_RATE	
0.1
PAYPAL_WPP_SIGNATURE	
u'********************'
SESSION_CACHE_ALIAS	
'default'
APP_DISQUS_NAME	
'iphonebackupextractor'
REDIS	
{'default': {'DB': 0, 'HOST': 'nj-db-3', 'PORT': 6379}}
SESSION_COOKIE_DOMAIN	
None
SESSION_COOKIE_NAME	
'sessionid'
EMAIL_BACKEND	
'django.core.mail.backends.smtp.EmailBackend'
AWS_STORAGE_BUCKET_NAME	
's.iphonebackupextractor.com'
TIME_INPUT_FORMATS	
('%H:%M:%S', '%H:%M:%S.%f', '%H:%M')
SECURE_REDIRECT_EXEMPT	
[]
DATABASES	
{'default': {'ATOMIC_REQUESTS': False,
             'AUTOCOMMIT': True,
             'CONN_MAX_AGE': 0,
             'ENGINE': 'django.db.backends.mysql',
             'HOST': 'nj-db-3',
             'NAME': 'iphonebe',
             'OPTIONS': {},
             'PASSWORD': u'********************',
             'PORT': '',
             'TEST': {'CHARSET': None,
                      'COLLATION': None,
                      'MIRROR': None,
                      'NAME': None},
             'TIME_ZONE': 'UTC',
             'USER': 'iphonebe'},
 'uds': {'ATOMIC_REQUESTS': False,
         'AUTOCOMMIT': True,
         'CONN_MAX_AGE': 0,
         'ENGINE': 'django.db.backends.mysql',
         'HOST': 'nj-db-3',
         'NAME': 'uds',
         'OPTIONS': {},
         'PASSWORD': u'********************',
         'PORT': '',
         'TEST': {'CHARSET': None,
                  'COLLATION': None,
                  'MIRROR': None,
                  'NAME': None},
         'TIME_ZONE': 'UTC',
         'USER': 'iphonebe'}}
EMAIL_SSL_KEYFILE	
u'********************'
BLOG_TRANSLATIONS	
True
FILE_UPLOAD_PERMISSIONS	
None
FILE_UPLOAD_HANDLERS	
('django.core.files.uploadhandler.MemoryFileUploadHandler',
 'django.core.files.uploadhandler.TemporaryFileUploadHandler')
TEMPLATE_CONTEXT_PROCESSORS	
('django.contrib.auth.context_processors.auth',
 'django.template.context_processors.debug',
 'django.template.context_processors.i18n',
 'django.template.context_processors.media',
 'django.template.context_processors.static',
 'django.template.context_processors.tz',
 'django.contrib.messages.context_processors.messages')
DEFAULT_CONTENT_TYPE	
'text/html'
UNDELETABLE_BASKET_PRODUCTS	
[1001, 10006, 10007, 10008]
APPEND_SLASH	
True
FIRST_DAY_OF_WEEK	
0
DATABASE_ROUTERS	
['reincubate_core.billing.routers.BillingRouter']
EMAIL_USE_SSL	
False
MEDIA_ROOT	
'../../../var/www-hosts/ipbe-site/docroot_collected/res/media'
JPMC_ACTIVE	
True
JPMC_USERNAME_VALIDATION	
True
YEAR_MONTH_FORMAT	
'F Y'
BILLING_EMAIL_RECEIPT_UTM_SOURCE	
'topreceipt'
STATICFILES_STORAGE	
'django.contrib.staticfiles.storage.StaticFilesStorage'
CACHES	
{'default': {'BACKEND': 'django.core.cache.backends.memcached.MemcachedCache',
             'KEY_PREFIX': u'********************',
             'LOCATION': 'nj-db-3:11211',
             'TIMEOUT': 3600}}
PASSWORD_HASHERS	
u'********************'
PAYPAL_DEBUG	
True
SESSION_COOKIE_PATH	
'/'
SIGNING_BACKEND	
'django.core.signing.TimestampSigner'
FLAVOURS	
('full', 'mobile', 'tablet')
BILLING_EMAIL_PENDING_UTM_SOURCE	
'toptxpending'
SECURE_CONTENT_TYPE_NOSNIFF	
False
MIDDLEWARE_CLASSES	
('django.middleware.common.CommonMiddleware',
 'django.contrib.sessions.middleware.SessionMiddleware',
 'django.contrib.auth.middleware.AuthenticationMiddleware',
 'django.contrib.messages.middleware.MessageMiddleware',
 'django.middleware.csrf.CsrfViewMiddleware',
 'django.middleware.locale.LocaleMiddleware',
 'reincubate_core.cms.middleware.SubdomainMiddleware',
 'reincubate_core.cms.middleware.AjaxMiddleware',
 'reincubate_core.cms.middleware.Custom403Middleware',
 'reincubate_core.cms.middleware.SSLRedirect',
 'reincubate_core.affiliate.middleware.AffiliateMiddleware',
 'trackback.middleware.PingbackUrlInjectionMiddleware',
 'reincubate_core.loadbal.middleware.BuildIdentificationMiddleware',
 'reincubate_core.billing.middleware.BasketMiddleware',
 'reincubate_core.profiles.middleware.LanguageRedirectMiddleware',
 'django_mobile.middleware.MobileDetectionMiddleware',
 'reincubate_core.cms.middleware.BetterMobileDetectionMiddleware',
 'django_mobile.middleware.SetFlavourMiddleware',
 'waffle.middleware.WaffleMiddleware')
USE_I18N	
True
THOUSAND_SEPARATOR	
','
BILLING_EMAIL_PDF_FILENAME_SUFFIX	
'Reincubate iPhone Backup Extractor'
LANGUAGE_COOKIE_NAME	
'lang'
SESSION_FILE_PATH	
None
DEFAULT_INDEX_TABLESPACE	
''
SECURE_SSL_HOST	
None
TEMPLATESADMIN_EDITHOOKS	
('templatesadmin.edithooks.dotbackupfiles.DotBackupFilesHook',
 'reincubate_core.cms.templateadmin.GitCommitHook')
BLOG_RIGHTS	
'Copyright &amp;copy; 2008 - 2012, Reincubate Ltd.'
JPMC_PRIVATE_KEY	
u'********************'
JPMC_MERCHANT_IDS	
{'EUR': {'ecomm': '237298', 'recurring': '237301'},
 'GBP': {'ecomm': '237294', 'moto': '237288', 'recurring': '237285'},
 'RUB': {'ecomm': '237268', 'recurring': '237274'},
 'USD': {'ecomm': '237339', 'recurring': '237334'}}
STATIC_HOST	
'stage-ipbe.reincubate.com'
TEMPLATE_LOADERS	
('django.template.loaders.filesystem.Loader',
 'django.template.loaders.app_directories.Loader')
WSGI_APPLICATION	
None
TEMPLATE_DEBUG	
True
X_FRAME_OPTIONS	
'SAMEORIGIN'
CSRF_COOKIE_NAME	
'csrftoken'
DEFAULT_BASKET_PRODUCTS	
[(1001, 1), (10006, 0), (10007, 0), (10008, 0)]
EMAIL_HOST_PASSWORD	
u'********************'
USE_X_FORWARDED_HOST	
False
AWS_S3_SECURE_URLS	
True
EMAIL_TIMEOUT	
None
BILLING_NEW_PDF_INVOICE	
True
ROSETTA_WSGI_AUTO_RELOAD	
True
SESSION_COOKIE_SECURE	
False
GOOGLEPLUS_URL	
'https://plus.google.com/+Reincubate'
SECURE_BROWSER_XSS_FILTER	
False
AB_TEST_WAFFLE_FLAG_NAME	
'repackage_test'
CSRF_COOKIE_DOMAIN	
None
FILE_CHARSET	
'utf-8'
DEBUG	
True
COMMENTS_APP	
'reincubate_core.captcha_comments'
LANGUAGES_ON	
True
LANGUAGE_COOKIE_DOMAIN	
None
AWS_ACCESS_KEY_ID	
u'********************'
AWS_CALLING_FORMAT	
<boto.s3.connection.SubdomainCallingFormat object at 0x2b81750>
INSTALLED_APPS	
('reincubate_core.auth',
 'django.contrib.auth',
 'django.contrib.contenttypes',
 'django.contrib.sessions',
 'django.contrib.sites',
 'django.contrib.admin',
 'django.contrib.sitemaps',
 'django_comments',
 'django.contrib.staticfiles',
 'reincubate_core',
 'reincubate_core.email_validation',
 'reincubate_core.cms',
 'reincubate_core.blog',
 'reincubate_core.captcha',
 'reincubate_core.captcha_comments',
 'reincubate_core.conf',
 'reincubate_core.lazy_social',
 'reincubate_core.merchant',
 'reincubate_core.profiles',
 'reincubate_core.udssclient',
 'reincubate_core.utils',
 'jpmc',
 'tagging',
 'reincubate_core.billing',
 'paypal.standard.ipn',
 'paypal.standard',
 'paypal.pro',
 'memcache_status',
 'rosetta',
 'modeltranslation',
 'trackback',
 'ttag',
 'reincubate_core.affiliate',
 'widget_tweaks',
 'raven.contrib.django',
 'renderform',
 'templatesadmin',
 'rimobile',
 'django_mobile',
 'ckeditor',
 'user_agents',
 'waffle')
LANGUAGES_BIDI	
('he', 'ar', 'fa', 'ur')
USE_L10N	
True
HIDE_DISQUS	
True
FORCE_HTTPS	
False
STATICFILES_DIRS	
('/var/www-hosts/ipbe-site/docroot',
 ('', '/var/www-hosts/ipbe-site/project/../project/../docroot/real_docroot'))
APP_SHORT_NAME	
'ipbe'
PREPEND_WWW	
False
SECURE_PROXY_SSL_HEADER	
None
BLOG_LOGO	
'http://s.iphonebackupextractor.com/res/i/windows-shot-small.jpg'
LANGUAGE_COOKIE_AGE	
None
MERCHANT_SETTINGS	
{'jpmc': {'MERCHANT_IDS': {'EUR': {'ecomm': '237298', 'recurring': '237301'},
                           'GBP': {'ecomm': '237294',
                                   'moto': '237288',
                                   'recurring': '237285'},
                           'RUB': {'ecomm': '237268', 'recurring': '237274'},
                           'USD': {'ecomm': '237339', 'recurring': '237334'}},
          'ORBITAL_PASSWORD': u'********************',
          'ORBITAL_USERNAME': 'T2270REIN',
          'PRIMARY_URL': 'https://orbitalvar1.paymentech.net/authorize',
          'SECONDRY_URL': 'https://orbitalvar2.paymentech.net/authorize'},
 'pay_pal': {'RECEIVER_EMAIL': 'aidan+sandbox@iphonebackupextractor.com',
             'WPP_PASSWORD': u'********************',
             'WPP_SIGNATURE': u'********************',
             'WPP_USER': 'aidan_api1.reincubate.com'}}
AWS_SECRET_ACCESS_KEY	
u'********************'
DEBUG_PROPAGATE_EXCEPTIONS	
False
INTERNAL_IPS	
('127.0.0.1',)
BLOG_APP_NAME	
'iPhone Backup Extractor'
SENTRY_DSN	
None
MONTH_DAY_FORMAT	
'F j'
LOGIN_URL	
'/login/'
SESSION_EXPIRE_AT_BROWSER_CLOSE	
False
RAVEN_CONFIG	
{u'auto_log_stacks': None,
 u'context': None,
 u'dsn': None,
 u'exclude_paths': None,
 u'include_paths': set(['ckeditor',
                        'django.contrib.admin',
                        'django.contrib.auth',
                        'django.contrib.contenttypes',
                        'django.contrib.sessions',
                        'django.contrib.sitemaps',
                        'django.contrib.sites',
                        'django.contrib.staticfiles',
                        'django_comments',
                        'django_mobile',
                        'jpmc',
                        'memcache_status',
                        'modeltranslation',
                        'paypal.pro',
                        'paypal.standard',
                        'paypal.standard.ipn',
                        'raven.contrib.django',
                        'reincubate_core',
                        'reincubate_core.affiliate',
                        'reincubate_core.auth',
                        'reincubate_core.billing',
                        'reincubate_core.blog',
                        'reincubate_core.captcha',
                        'reincubate_core.captcha_comments',
                        'reincubate_core.cms',
                        'reincubate_core.conf',
                        'reincubate_core.email_validation',
                        'reincubate_core.lazy_social',
                        'reincubate_core.merchant',
                        'reincubate_core.profiles',
                        'reincubate_core.udssclient',
                        'reincubate_core.utils',
                        'renderform',
                        'rimobile',
                        'rosetta',
                        'tagging',
                        'templatesadmin',
                        'trackback',
                        'ttag',
                        'user_agents',
                        'waffle',
                        'widget_tweaks']),
 u'key': '7e043950308c89b9228b908194c2ee53',
 u'list_max_length': None,
 u'name': None,
 u'processors': None,
 u'project': None,
 u'public_key': None,
 u'secret_key': None,
 u'servers': None,
 u'site': None,
 u'string_max_length': None,
 u'timeout': None}
WAFFLE_MAX_AGE	
5184000
TIME_FORMAT	
'P'
APP_DISQUS_URL	
'http://www.iphonebackupextractor.com/'
GEOIP_PATH	
'/usr/share/GeoIP/GeoIP.dat'
BLOG_WYSIWYG	
False
APP_PAYPAL_LICENSE_SUPPORT	
['iPhone Backup Extractor License Support']
AUTH_USER_MODEL	
'auth.User'
DATE_INPUT_FORMATS	
('%Y-%m-%d',
 '%m/%d/%Y',
 '%m/%d/%y',
 '%b %d %Y',
 '%b %d, %Y',
 '%d %b %Y',
 '%d %b, %Y',
 '%B %d %Y',
 '%B %d, %Y',
 '%d %B %Y',
 '%d %B, %Y')
ROSETTA_UWSGI_AUTO_RELOAD	
True
REVIEW_URL	
'http://download.cnet.com/iPhone-Backup-Extractor/3000-18553_4-75373326.html#rateit'
SESSION_SERIALIZER	
'django.contrib.sessions.serializers.JSONSerializer'
AUTHENTICATION_BACKENDS	
['reincubate_core.auth.auth_backend.EmailLoginBackend']
APP_PAYPAL_ITEMS	
['iPhone Backup Extractor']
AB_TEST_DEFAULT_BASKET	
[(10006, 1), (10007, 0), (10008, 0)]
REDIS_SSEQUEUE_CONNECTION_SETTINGS	
{'db': 0, 'location': 'nj-db-3:6379'}
PASSWORD_RESET_TIMEOUT_DAYS	
u'********************'
JPMC_SECONDRY_URL	
'https://orbitalvar2.paymentech.net/authorize'
CACHE_MIDDLEWARE_ALIAS	
'default'
SESSION_SAVE_EVERY_REQUEST	
False
PAYPAL_WPP_PASSWORD	
u'********************'
NUMBER_GROUPING	
0
DYNAMIC_HOST	
'stage-ipbe.reincubate.com'
JPMC_ORBITAL_USERNAME	
'T2270REIN'
SESSION_ENGINE	
'django.contrib.sessions.backends.db'
DEFAULT_FILE_STORAGE	
'storages.backends.s3boto.S3BotoStorage'
CSRF_FAILURE_VIEW	
'django.views.csrf.csrf_failure'
CSRF_COOKIE_PATH	
'/'
LOGIN_REDIRECT_URL	
'/manage-licenses/'
APP_ADSENSE_CONVERSION_ID	
'1039638349'
PROJECT_ROOT	
'/var/www-hosts/ipbe-site/project'
APP_GA_ACCOUNT	
'UA-2156704-13'
BLOG_ID	
'http://www.iphonebackupextractor.com/blog/'
DECIMAL_SEPARATOR	
'.'
CACHE_MIDDLEWARE_KEY_PREFIX	
u'********************'
LOCALE_PATHS	
('/var/www-hosts/ipbe-site/project/../project/../conf/locale',)
MODELTRANSLATION_DEFAULT_LANGUAGE	
'en'
TEMPLATE_STRING_IF_INVALID	
''
DISALLOWED_USER_AGENTS	
()
NO_SOCIAL_AUTH	
True
OVERRIDE_INVOICE_ADMIN_CHANGELIST_TEMPLATE	
'admin/invoice/change_list.html'
BLOG_TWITTER	
'iphonebackups'
LOGOUT_URL	
'/accounts/logout/'
EMAIL_USE_TLS	
True
TEMPLATE_DIRS	
()
FIXTURE_DIRS	
['/var/www-hosts/ipbe-site/project/../project/project/fixtures']
EMAIL_HOST	
'smtp.mandrillapp.com'
REDIS_SSEQUEUE_CHANEL_NAME	
'sse_billing_stream'
DATE_FORMAT	
'N j, Y'
BLOG_IMAGE_URL	
' https://s3.amazonaws.com/s.iphonebackupextractor.com/res/blog/i/download-iphone-backup-extractor-windows-mac.png'
TEMPLATESADMIN_TEMPLATE_DIRS	
('/var/www-hosts/ipbe-site/project/../project/../apps/',)
APP_SUPPORT_EMAIL	
'support@reincubate.com'
BING_PPC_ACTION_ID	
164800
QUESTIONS_ON_THANKYOU_PAGE	
True
LANGUAGE_COOKIE_PATH	
'/'
DSNS	
{'awdit-desktop': 'https://31011a1b85514d2db611ee2e8875d872:124981348602439b9f12b34edb43833f@app.getsentry.com/3017',
 'bbbe': 'https://72cb2379f3df41929f896e8bb4c99817:977fbfba751b4a85a59cd301f4f29069@app.getsentry.com/3015',
 'convertervideo': 'https://4d066b81981b48ad93eabeac54e5e573:57da818416db47599ae45eb3437a7ea1@app.getsentry.com/3019',
 'dmge': 'https://650120a552ae448ea6c1a4106030b4d9:6bbaeffbd21b45198ca06c606b24cabd@app.getsentry.com/3016',
 'filesrecover': 'https://ff7be3a1098e4f03b073762e4e93578a:9b99093e46d3498097471d463b9b9c8c@app.getsentry.com/3020',
 'ipbe': 'https://9a04512ee4164773b054763498051c58:6037c5cd93db47e98bfd2c3f1aaf871e@app.getsentry.com/3000',
 'tunepc': 'https://d42a4570c21948a08fe2d195c0365823:5263e7d0b6034a558b87c91b42e7182f@app.getsentry.com/3018'}
DEFAULT_EXCEPTION_REPORTER_FILTER	
'django.views.debug.SafeExceptionReporterFilter'
ADMINS	
(('Sysadmin', 'sysadmin@reincubate.com'),)
FORMAT_MODULE_PATH	
None
DEFAULT_FROM_EMAIL	
'webmaster@localhost'
SECURE_HSTS_INCLUDE_SUBDOMAINS	
False
BLOG_TITLE_SUFFIX	
' - iPhone Backup Extractor Blog'
WAFFLE_SECURE	
False
APP_ADSENSE_CONVERSION_CODE	
'iz8yCNWb5QMQzb7e7wM'
MEDIA_URL	
'/res/media/'
DATETIME_FORMAT	
'N j, Y, P'
APP_KEY_NAME	
u'********************'
CKEDITOR_CONFIGS	
{'default': {'resize_dir': 'both', 'toolbar': 'Advanced'}}
BLOG_TITLE_PREFIX	
''
SITE_ID	
1
APP_INSTALL_VIDEO_URL	
'http://www.youtube.com/embed/BS8vT7hJO0M'
ALLOWED_INCLUDE_ROOTS	
()
JPMC_PRIMARY_URL	
'https://orbitalvar1.paymentech.net/authorize'
LOGGING	
{'disable_existing_loggers': True,
 'filters': {'require_debug_false': {'()': 'django.utils.log.RequireDebugFalse'}},
 'formatters': {'sensitive': {'()': 'reincubate_core.utils.logging.StripSensitiveInformation'},
                'standard': {'datefmt': '%d/%b/%Y %H:%M:%S',
                             'format': '[%(asctime)s] %(levelname)s [%(name)s:%(lineno)s] %(message)s'}},
 'handlers': {'console': {'class': 'logging.StreamHandler',
                          'formatter': 'sensitive',
                          'level': 'DEBUG'},
              'mail_admins': {'class': 'django.utils.log.AdminEmailHandler',
                              'filters': ['require_debug_false'],
                              'level': 'ERROR'},
              'sentry': {'class': 'raven.contrib.django.raven_compat.handlers.SentryHandler',
                         'level': 'ERROR'}},
 'loggers': {'jpmc': {'handlers': ['console'],
                      'level': 'DEBUG',
                      'propagate': True},
             'sentry.errors': {'handlers': ['mail_admins'],
                               'level': 'ERROR',
                               'propagate': True}},
 'root': {'handlers': ['sentry', 'console'], 'level': 'DEBUG'},
 'version': 1}
YOUTUBE_URL	
'https://www.youtube.com/user/ReincubateTV'
SHORT_DATE_FORMAT	
'm/d/Y'
SECRET_KEY	
u'********************'
TEMPLATES	
[{'BACKEND': 'django.template.backends.django.DjangoTemplates',
  'DIRS': ['/var/www-hosts/ipbe-site/project/../apps/cms/templates',
           '/var/www-hosts/ipbe-site/project/../apps/rimobile/templates'],
  'OPTIONS': {'context_processors': ('django.contrib.auth.context_processors.auth',
                                     'django.core.context_processors.debug',
                                     'django.core.context_processors.i18n',
                                     'django.core.context_processors.media',
                                     'django.core.context_processors.request',
                                     'django.contrib.messages.context_processors.messages',
                                     'reincubate_core.cms.contextprocessors.settings_context_processor',
                                     'reincubate_core.billing.contextprocessors.billing_context_processor'),
              'loaders': [('django.template.loaders.filesystem.Loader',),
                          ('django.template.loaders.app_directories.Loader',)]}}]
LANG_RE	
'^(?:(?P<lang>(fr|de|jp|zh|es))/)?'
TEST_RUNNER	
'django.test.runner.DiscoverRunner'
PINGBACK_RESOLVERS	
('reincubate_core.blog.pingback_resolver.pingback_resolver',)
MODELTRANSLATION_LANGUAGES	
('en', 'de', 'es', 'fr', 'ja', 'zh-cn')
VAT_ENABLED	
True
AB_TEST_COOKIE_NAME	
'repackage_test'
IGNORABLE_404_URLS	
()
SECURE_SSL_REDIRECT	
False
TIME_ZONE	
'UTC'
ADDITIONAL_TABLET_DEVICE_FAMILIES	
('Nexus 7', 'Nexus 10')
FILE_UPLOAD_MAX_MEMORY_SIZE	
2621440
SSL_STATIC_HOST	
's.iphonebackupextractor.com'
CAPTCHA_NOISE_FUNCTIONS	
[]
SEND_PASSWORD_EMAIL	
u'********************'
BLOG_TITLE	
'iPhone Backup Extractor Blog: The iPhone Backup Extractor'
DEFAULT_TABLESPACE	
''
SESSION_COOKIE_HTTPONLY	
True
MIGRATION_MODULES	
{}
SESSION_COOKIE_AGE	
1209600
SETTINGS_MODULE	
'settings'
USE_ETAGS	
False
BLOG_IMAGE_HREF	
'http://www.iphonebackupextractor.com/free-download/'
LANGUAGES	
(('en', 'English'),
 ('de', 'German'),
 ('es', 'Spanish'),
 ('fr', 'French'),
 ('ja', 'Japanese'),
 ('zh-cn', 'Simplified Chinese'))
FILE_UPLOAD_TEMP_DIR	
None
CSRF_COOKIE_AGE	
31449600
STATIC_URL	
'/res/'
EMAIL_PORT	
587
USE_TZ	
False
SHORT_DATETIME_FORMAT	
'm/d/Y P'
JPMC_NUM_RETRIES	
1
TEST_NON_SERIALIZED_APPS	
[]
AB_TEST_WAFFLE_COOKIE_NAME	
'dwf_repackage_test'
BLOG_ROOT	
'http://www.iphonebackupextractor.com'
PAYPAL_RECEIVER_EMAIL	
'aidan@iphonebackupextractor.com'
ABSOLUTE_URL_OVERRIDES	
{}
SILENCED_SYSTEM_CHECKS	
[]
JPMC_BIN_ID	
'000001'
DSN_HANDLE_FOR_THIS_APP	
'ipbe'
FACEBOOK_URL	
'https://www.facebook.com/reincubate'
JPMC_TERMINAL_ID	
'001'
CACHE_MIDDLEWARE_SECONDS	
600
EMAIL_SSL_CERTFILE	
None
CSRF_COOKIE_HTTPONLY	
False
DATETIME_INPUT_FORMATS	
('%Y-%m-%d %H:%M:%S',
 '%Y-%m-%d %H:%M:%S.%f',
 '%Y-%m-%d %H:%M',
 '%Y-%m-%d',
 '%m/%d/%Y %H:%M:%S',
 '%m/%d/%Y %H:%M:%S.%f',
 '%m/%d/%Y %H:%M',
 '%m/%d/%Y',
 '%m/%d/%y %H:%M:%S',
 '%m/%d/%y %H:%M:%S.%f',
 '%m/%d/%y %H:%M',
 '%m/%d/%y')
FORCE_SCRIPT_NAME	
None
VAT_SIMPLE	
True
LOGGING_CONFIG	
'logging.config.dictConfig'
EMAIL_HOST_USER	
'aidan@reincubate.com'
