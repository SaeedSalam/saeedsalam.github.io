## Setting up a custom domain on Github Pages

As you may already know, am _hosting_ this blog on Github Pages, my blog address were like ``<myusername>.github.io`` which actually looks bit unprofessional, and as i already had registered a domain under my name, saeedsalam.com, i wanted to map that to this blog.

The process were pretty simple, my domain were ready and up in 10 mins!

Just go to your **Domain Registrar**, browser DNS settings page, and add following ``A`` & ``AAAA`` records there.

``A`` records:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

``AAAA`` records:
```
2606:50c0:8000::153
2606:50c0:8001::153
2606:50c0:8002::153
2606:50c0:8003::153
```

This will map main domain (saeedsalam.com) to the Github Pages, but if we want to redirect `www` version as well, we will need to add a `CNAME` record as well.
Just add a CNAME record as follows:

`www.yourdomain.com` or just `WWW` to `<yourusername>.github.io`
change _yourusername_ to your GitHub username you used to create the current Page.

Here is a screenshot of my DNS settings:

![image](https://github.com/SaeedSalam/saeedsalam.github.io/assets/11427342/f12bf1f0-2bb4-4785-b20d-4aaea290db55)

After saving the DNS settings, just head over to Github again, go to the repo you want to add the domain, go to ``Settings`` -> ``Pages`` (on the left sidebar)

Scroll down to `Custom Domain` section.

Enter your domain name there, and click "Save", _voila_! your domain name is ready.

Note: for some domains, it may take some hours to propagate the DNS changes, so no need to panic if it doesn't work on the fly. Though 99% time, it will be ready in 5-10 mins.

Once that's ready, do check the ``Enforce HTTPS`` checkbox right below. That will redirect http to https.

That's all. I hope you find this helpful. See ya later!
