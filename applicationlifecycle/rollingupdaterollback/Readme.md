RollingUpdateStrategy:  25% max unavailable, 25% max surge

kubectl rollout history deployment/frontend

kubectl rollout status deployment/frontend

kubectl set image deployment/name \
                        nginx:1.27


kubectl rollout undo deployment/frontend