# api documentation for  [instagram-node (v0.5.8)](https://github.com/teleportd/instagram-node)  [![npm package](https://img.shields.io/npm/v/npmdoc-instagram-node.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-instagram-node) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-instagram-node.svg)](https://travis-ci.org/npmdoc/node-npmdoc-instagram-node)
#### Simple Instagram driver for Node.js

[![NPM](https://nodei.co/npm/instagram-node.png?downloads=true)](https://www.npmjs.com/package/instagram-node)

[![apidoc](https://npmdoc.github.io/node-npmdoc-instagram-node/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-instagram-node_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-instagram-node/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-instagram-node/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-instagram-node/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Anthony MOI",
        "email": "anthony@teleportd.com",
        "url": "https://github.com/n1t0"
    },
    "bugs": {
        "url": "https://github.com/teleportd/instagram-node/issues"
    },
    "dependencies": {
        "colors": "0.6.0-1",
        "fwk": "1.0.x"
    },
    "description": "Simple Instagram driver for Node.js",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "7317aa23f816654c0b003ace51d81a509af5ecbf",
        "tarball": "https://registry.npmjs.org/instagram-node/-/instagram-node-0.5.8.tgz"
    },
    "engines": {
        "node": ">=v0.6.0"
    },
    "gitHead": "81fee38a2636de5c4e814382968eb50ca4a5d5e1",
    "homepage": "https://github.com/teleportd/instagram-node",
    "keywords": [
        "instagram",
        "node",
        "ig",
        "driver"
    ],
    "main": "./lib/instagram",
    "maintainers": [
        {
            "name": "n1t0",
            "email": "anthony@teleportd.com"
        }
    ],
    "name": "instagram-node",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/teleportd/instagram-node.git"
    },
    "scripts": {},
    "version": "0.5.8"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module instagram-node](#apidoc.module.instagram-node)
1.  [function <span class="apidocSignatureSpan">instagram-node.</span>instagram (spec, my)](#apidoc.element.instagram-node.instagram)



# <a name="apidoc.module.instagram-node"></a>[module instagram-node](#apidoc.module.instagram-node)

#### <a name="apidoc.element.instagram-node.instagram"></a>[function <span class="apidocSignatureSpan">instagram-node.</span>instagram (spec, my)](#apidoc.element.instagram-node.instagram)
- description and source-code
```javascript
instagram = function (spec, my) {
  var _super = {};
  my = my || {};
  spec = spec || {};

  my.limit = null;
  my.remaining = null;
  my.agent = spec.agent;
  my.host = spec.host || 'https://api.instagram.com';
  my.port = spec.port || 443;
  my.enforce_signed_requests = spec.enforce_signed_requests || false;

  // public
  var use;<span class="apidocCodeCommentSpan">                              /* use(spec);                                       */
</span>
  var user;                             /* user(user_id, cb);                               */
  var user_self_feed;                   /* user_self_feed(options, cb);                     */
  var user_media_recent;                /* user_media_recent(user_id, options, cb);         */
  var user_self_media_recent;           /* user_self_media_recent(options, cb);             */
  var user_self_liked;                  /* user_self_liked(options, cb);                    */
  var user_search;                      /* user_search(query, options, cb);                 */

  var user_follows;                     /* user_follows(user_id, cb);                       */
  var user_followers;                   /* user_followers(user_id, cb);                     */
  var user_self_requested_by;           /* user_self_requested_by(cb);                      */
  var user_relationship;                /* user_relationship(user_id, cb);                  */
  var set_user_relationship;            /* set_user_relationship(user_id, action, cb);      */

  var media;                            /* media(media_id, cb);                             */
  var media_shortcode;                  /* media_shortcode(media_shortcode, cb);            */
  var media_search;                     /* media_search(lat, lng, options, cb);             */
  var media_popular;                    /* media_popular(cb);                               */

  var comments;                         /* comments(media_id, cb);                          */
  var add_comment;                      /* add_comment(media_id, text, cb);                 */
  var del_comment;                      /* del_comment(media_id, comment_id, cb);           */

  var likes;                            /* likes(media_id, cb);                             */
  var add_like;                         /* add_like(media_id, cb);                          */
  var del_like;                         /* del_like(media_id, cb);                          */

  var tag;                              /* tag(tag, cb);                                    */
  var tag_media_recent;                 /* tag_media_recent(tag, options, cb);              */
  var tag_search;                       /* tag_search(query, cb);                           */

  var location;                         /* location(location_id, cb);                       */
  var location_media_recent;            /* location_media_recent(location_id, options, cb); */
  var location_search;                  /* location_search(spec, options, cb);              */

  var geography_media_recent;           /* geography_media_recent(id, options, cb);         */

  var subscriptions;                    /* subscriptions(cb);                               */
  var del_subscription;                 /* del_subscription(options, cb);                   */
  var add_tag_subscription;             /* add_tag_subscription(tag, cb_url, cb);           */
  var add_geography_subscription;       /* add_geography_subscription(lat, lng, radius, cb_url, cb); */
  var add_user_subscription;            /* add_user_subscription(cb_url, cb);               */
  var add_location_subscription;        /* add_location_subscription(id, cb_url, cb);       */

  var get_authorization_url;            /* get_authorization_url(redirect_uri, permissions);*/
  var authorize_user;                   /* authorize_user(code, redirect_uri, cb);          */

  var oembed;                           /* oembed(url, cb);                             */

  // private
  var call;                             /* call(method, path, params, cb, retry);           */
  var handle_error;                     /* hand ...
```
- example usage
```shell
...
## How it works

* First of all, you need to authentify. You can use 'client_id/client_secret' from the app you are building, or an 'access_token
' from
a user that use your app.
* **Some features need an access_token to work**

'''javascript
var ig = require('instagram-node').instagram();

// Every call to 'ig.use()' overrides the 'client_id/client_secret'
// or 'access_token' previously entered if they exist.
ig.use({ access_token: 'YOUR_ACCESS_TOKEN' });
ig.use({ client_id: 'YOUR_CLIENT_ID',
         client_secret: 'YOUR_CLIENT_SECRET' });
'''
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
