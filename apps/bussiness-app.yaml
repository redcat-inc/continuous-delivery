apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: bussiness-app
  namespace: argocd
spec:
  project: default
  source:
    repoURL: 'https://github.com/redcat-inc/continious-delivery'
    targetRevision: master
    path: bussiness-app
  destination:
    server: 'https://kubernetes.default.svc'
    namespace: bussiness-app
  syncPolicy:
    automated:
      prune: true
      selfHeal: true
    syncOptions:
      - CreateNamespace=true
