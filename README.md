# WebToApp Android Template

Este repositório contém o template Android para o serviço WebToApp.

## Como funciona

1. O workflow `build-android.yml` é acionado via `workflow_dispatch`
2. Os parâmetros (URL, nome do app, package name, ícone) são passados
3. O APK e AAB são gerados automaticamente
4. Os artefatos ficam disponíveis para download

## Parâmetros do Workflow

- `app_url`: URL do site a ser convertido em app
- `app_name`: Nome do aplicativo
- `package_name`: Nome do pacote (ex: com.exemplo.meuapp)
- `icon_url`: URL do ícone (opcional)
- `build_id`: ID do build para callback
- `callback_url`: URL para notificação do status

## Estrutura do Projeto

```
├── app/
│   ├── src/main/
│   │   ├── java/com/webtoapp/template/
│   │   │   └── MainActivity.kt
│   │   ├── res/
│   │   │   ├── values/
│   │   │   └── mipmap-*/
│   │   └── AndroidManifest.xml
│   └── build.gradle
├── .github/workflows/
│   └── build-android.yml
└── build.gradle
```

## Requisitos

- GitHub Actions habilitado
- Repositório configurado como privado (recomendado)
