# Calendário Mnemônico

Calculadora mental de dias da semana usando regras mnemônicas do calendário gregoriano.

<p align="center">
  <img src="icons/icon-512.png" width="128" alt="App Icon">
</p>

## Regras

| Mês | Jan | Fev | Mar | Abr | Mai | Jun | Jul | Ago | Set | Out | Nov | Dez |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| Offset | 0 | 3 | 3 | 6 | 1 | 4 | 6 | 2 | 5 | 0 | 3 | 5 |

- **Fórmula**: `dia_semana = (código_ano + offset_mês + dia) mod 7`
- **+5 a cada 4 anos** (3 comuns × 1 + 1 bissexto × 2 = 5)
- **Ciclo completo a cada 28 anos** (5 × 7 = 35 ≡ 0 mod 7)
- **Exceção**: centenários não-quadricentenários quebram o ciclo

## Instalar no iOS

1. Acesse a página pelo Safari: `https://SEU_USUARIO.github.io/calendario-mnemonico/`
2. Toque no botão **Compartilhar** (⬆️)
3. Selecione **Adicionar à Tela de Início**
4. Confirme o nome e toque em **Adicionar**

O app funciona offline após a primeira visita.

## Deploy no GitHub Pages

1. Crie um repositório no GitHub (ex: `calendario-mnemonico`)
2. Faça push de todos os arquivos deste diretório
3. Vá em **Settings → Pages → Source** e selecione `main` branch
4. Acesse `https://SEU_USUARIO.github.io/calendario-mnemonico/`

```bash
git init
git add .
git commit -m "Calendário Mnemônico PWA"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/calendario-mnemonico.git
git push -u origin main
```

## Estrutura

```
├── index.html              # App completo (React inline, sem build)
├── manifest.json           # PWA manifest
├── sw.js                   # Service worker (cache offline)
├── icons/
│   ├── apple-touch-icon.png  # 180×180 ícone iOS
│   ├── icon-192.png          # 192×192 PWA
│   ├── icon-512.png          # 512×512 PWA
│   └── favicon.ico           # Favicon
└── README.md
```

## Licença

Uso pessoal. Faça o que quiser com ele.
