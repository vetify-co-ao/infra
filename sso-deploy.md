# Deploy file email-body-template.html

Create the email-body-template-file config map as below:

```bash
kubectl -n vetify create configmap sso-email-body-template --from-file=email_body_template.html=sso-email-body-template.html
```

Create the email secret as below:

```bash
kubectl -n vetify create secret generic sso-email-secret --from-literal=sso.key='email_secret'
```

Create JWK key file as below:

```bash
kubectl -n vetify create configmap sso-jwk-file --from-file=jwk.json=sso-jwk.json
```
