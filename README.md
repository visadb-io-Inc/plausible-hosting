Update API Scopes

```
docker compose exec plausible_db psql -U postgres -d plausible_db -c "UPDATE API_KEYS SET scopes = ARRAY['stats:read:*', 'sites:provision:*'];"
```

Update API Limits

```
docker compose exec plausible_db psql -U postgres -d plausible_db -c "UPDATE API_KEYS SET hourly_request_limit = 800000000"
```
