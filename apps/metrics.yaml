apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: metrics
  namespace: argocd
spec:
  project: default
  source:
    repoURL: 'https://github.com/redcat-inc/continious-delivery'
    targetRevision: master
    path: charts/metrics
  destination:
    server: 'https://kubernetes.default.svc'
    namespace: metrics
  syncPolicy:
    automated:
      prune: true
      selfHeal: true
    syncOptions:
      - CreateNamespace=true
