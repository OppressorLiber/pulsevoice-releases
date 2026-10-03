# PulseVoice para Windows


Conversas privadas, chamadas de voz e vídeo e reuniões para até 8 pessoas. Aplicativo experimental para Windows 10/11 de 64 bits.


## Download


[Baixar PulseVoice.exe](https://github.com/OppressorLiber/pulsevoice-releases/releases/latest/download/PulseVoice.exe) · [Todas as versões](https://github.com/OppressorLiber/pulsevoice-releases/releases)


Abra o executável em uma pasta com permissão de escrita. Não precisa instalar Python.


## Conversas e perfil


Em **Perfil**, escolha foto, nome, descrição e status; use **Copiar meu código** e compartilhe o código `PVF-XXXX-XXXX-XXXX-XXXX` com a pessoa que deseja adicionar. Depois de aceitar o contato, vocês podem trocar mensagens e iniciar uma chamada. Desde a versão 0.7, com ambos os aplicativos conectados, a outra pessoa recebe um aviso com som e **Atender / Recusar**. O convite também aparece no chat. Os avisos expiram em 60 segundos; **Não perturbar** recusa novas chamadas. O aplicativo precisa permanecer aberto para receber o aviso.


O histórico e a identidade ficam no computador. Mensagens pendentes são enviadas quando os dois contatos estiverem conectados. Exporte um backup protegido por senha em **Perfil** antes de trocar de computador. Não há recuperação por e-mail nem sincronização entre dispositivos.


## Novidades da versão 0.9

- **Código de amigo curto:** 23 caracteres, preservado ao trocar nome ou foto. Cole em **+ / Adicionar amigo** ou na busca e pressione Enter. Convites antigos continuam válidos. A busca requer internet e a pessoa precisa abrir a versão 0.9 com o nome salvo para publicar o código.
- **Perfil na chamada:** clique no nome ou na foto do participante para **Adicionar amigo** ou **Aceitar amizade**. Depois da aceitação, **Enviar mensagem** abre o chat privado enquanto a chamada continua. Volume, silêncio local e destaque ficam no mesmo painel.
- **Chamada aberta aos amigos:** o criador ativa **Mostrar chamada aos amigos**. Na conversa dos amigos aceitos aparece **Entrar na chamada**, sem convite individual. Uma chamada de duas pessoas passa a aceitar até oito; desligar a opção esconde a entrada e conserva os participantes. Sair encerra a chamada e desativa a opção. Invisível e perda de conexão escondem o anúncio.

Atualizem todos os participantes para 0.9 para usar os novos atalhos e a expansão de chamadas. Reuniões continuam com **até 8 pessoas**, sem TURN.

O diretório de códigos guarda somente chave pública e nome criptografados no serviço de testes; quem conhece o código pode consultá-los. Mensagens, fotos e convites de chamada não são guardados nesse diretório. A amizade precisa ser aceita para liberar a conversa. O serviço pode reiniciar e perder registros; abrir o aplicativo novamente publica o código. O histórico permanece local.

Validação do executável final: três clientes temporários neste Windows, serviço público real, busca de código, amizade e conversa privada pelo perfil durante a chamada, entrada pelo botão sem convite individual, WebRTC com áudio sintético, reconexão e anúncios encerrados/expirados. Não valida computadores físicos em redes diferentes nem a meta de 10 ms.

## Reuniões


Em **Reuniões**, crie uma sala e compartilhe o convite. Dentro dela, **Dispositivos** permite escolher microfone, fones e webcam, incluindo **LumaCam Camera** quando a webcam virtual estiver ativa. O criador precisa permanecer conectado. Use fones para evitar eco.


A grade tem fotos, destaque de quem fala e participante fixado por duplo clique. Pelo painel do participante, ajuste o volume de 0 a 200% ou **Silenciar só para mim**. O indicador de RTT e perda estimada não mede o atraso completo da voz. As reuniões continuam limitadas a **8 pessoas**.


## Correção da conexão na versão 0.8.1

A criação da sala confirma a inscrição no serviço e ignora respostas de tentativas antigas. Após uma queda, o aplicativo tenta reconectar automaticamente e, se necessário, alterna entre as portas TLS do mesmo serviço. A presença e os convites pendentes são atualizados quando a conexão volta. Uma chamada direta saudável continua durante a interrupção da sinalização. O bate-papo mostra que está reconectando e conserva o rascunho quando o envio falha. Se o serviço estiver totalmente indisponível, a criação mostra o erro e permite tentar novamente.

A correção foi validada no executável final com dois clientes no mesmo Windows, serviço público real, voz sintética via WebRTC, reconexão e uma interrupção de sinalização de 24 segundos. Esses testes não validam dois PCs em redes diferentes.

## Captura e atualização da versão 0.8


- Captura nativa do Windows com **cursor incluído**, inclusive sobre conteúdo parado, para janela ou monitor.
- Seletor com **30 FPS · mais fluido** e **15 FPS · econômico**, com imagem até 960 × 540. Requer Windows 10 versão 2004 (build 19041) ou mais recente para compartilhar.
- Só o último quadro aguarda exibição, evitando uma fila de imagens atrasadas.
- Correção da reabertura automática após atualizar, que podia falhar ao carregar python312.dll de uma pasta temporária já removida.


**Compartilhar tela** abre a escolha do alvo e só começa ao clicar em **Compartilhar**; **Parar tela** encerra. A webcam fica pausada e pode voltar automaticamente depois. O microfone continua disponível. O áudio do computador não é compartilhado.


FPS é uma meta; computador e rede afetam o resultado. Os testes locais receberam vídeo perto de 30 FPS entre dois clientes. Oito clientes concentrados num único processo com áudio contínuo sobrecarregaram o teste; use 15 FPS se compartilhar prejudicar o áudio. Isso não valida oito computadores físicos.


## Atualizações


Abra **Versões**, baixe a versão disponível e, fora de uma chamada, escolha **Instalar e reiniciar**. O download é verificado por SHA-256 informado pelo GitHub; o executável anterior fica como backup.


**Ao atualizar uma versão anterior para 0.8:** o instalador antigo pode mostrar o erro de DLL uma última vez mesmo tendo substituído o arquivo. Feche a mensagem e abra PulseVoice.exe manualmente. Você também pode baixar o EXE novo, fechar o aplicativo antigo e abrir o novo diretamente. Perfil e conversas permanecem na pasta de dados do Windows. Atualizações iniciadas pela versão 0.8 usam o reinício corrigido.


## Limites do protótipo


A conexão usa o serviço público gratuito de testes Mosquitto para sinalização e mensagens criptografadas, com histórico local. Esse serviço pode sofrer interrupções. Voz e vídeo usam conexão direta, sem servidor TURN; algumas redes e CGNAT podem impedir chamadas. A meta de 10 ms depende da rede e dos equipamentos e não é garantida.


Este repositório contém apenas downloads e documentação. O código-fonte permanece local. Não publique credenciais, backups, convites ou conversas nos relatos de problemas.

