# Mining Clicker Simulator: pacote do app

## Como colocar no ar (grátis)
1. Netlify: entre em app.netlify.com, arraste esta pasta inteira na área "Deploy". Você recebe um link.
   GitHub Pages: envie os arquivos para um repositório e ative Settings > Pages.
2. No celular, abra o link e use "Adicionar à tela inicial". O jogo vira um app com ícone.

## Como administrar sem atrapalhar os jogadores
- Ajustes de equilíbrio e avisos: edite o config.json e envie de novo.
  dm = dano, cm = moedas, hp = vida dos blocos, ep = preço dos ovos, up = preço das melhorias,
  rb = custo do renascimento, msg = aviso mostrado no topo do jogo para todos.
  Os jogadores recebem a mudança em até 5 minutos, sem recarregar.
- Nova versão do jogo: envie o novo index.html. Quem estiver jogando não é interrompido;
  a versão nova carrega na próxima vez que a pessoa abrir o app. O progresso fica salvo no aparelho.
- Ao criar novas melhorias ou itens, mantenha os nomes antigos para não quebrar saves existentes.

## Observações
- Não existe aba ADM nesta versão. Só você mexe no jogo, pelo config.json.
- O ranking online só funciona dentro do claude.ai. Neste pacote ele aparece como indisponível.

## App de loja (opcional)
  npm init -y && npm i @capacitor/core @capacitor/cli
  npx cap init "Mining Clicker" com.seunome.miningclicker --web-dir=.
  npm i @capacitor/android && npx cap add android && npx cap open android
