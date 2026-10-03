# PulseVoice para Windows

Conversas privadas, chamadas de voz e vídeo e reuniões para até 8 pessoas. Aplicativo experimental para Windows 10/11 de 64 bits.

## Download

[Baixar PulseVoice.exe](https://github.com/OppressorLiber/pulsevoice-releases/releases/latest/download/PulseVoice.exe) · [Todas as versões](https://github.com/OppressorLiber/pulsevoice-releases/releases)

Abra o executável em uma pasta com permissão de escrita. Não precisa instalar Python.

## Conversas e perfil

Desde a versão 0.6, as conversas ficam na lateral esquerda. Em **Perfil**, escolha foto, nome, descrição e status; copie seu convite e compartilhe com a pessoa que deseja adicionar. Depois de aceitar o contato, vocês podem trocar mensagens e iniciar uma chamada. Com ambos os aplicativos na versão 0.7 e conectados, a outra pessoa recebe um aviso com som e botões **Atender / Recusar**. O convite também aparece no chat. Os avisos expiram em 60 segundos; **Não perturbar** recusa novas chamadas. O aplicativo precisa permanecer aberto para receber o aviso.

O histórico e a identidade ficam no computador. Mensagens pendentes são enviadas quando os dois contatos estiverem conectados. Exporte um backup protegido por senha em **Perfil** para preservar sua identidade e conversas antes de trocar de computador. Não há recuperação por e-mail nem sincronização entre dispositivos.

## Reuniões

Em **Reuniões**, crie uma sala e compartilhe o convite. Dentro dela, **Dispositivos** permite escolher microfone, fones e webcam, incluindo **LumaCam Camera** quando a webcam virtual estiver ativa. O criador precisa permanecer conectado. Use fones para evitar eco.

## Novidades da versão 0.7

- Grade adaptável com fotos de perfil, destaque de quem fala e participante fixado por duplo clique ou pelo painel de controles.
- Volume individual de 0 a 200% e **Silenciar só para mim**, pelo ícone de controles de cada participante.
- **Compartilhar tela** permite escolher uma janela ou monitor; **Parar tela** encerra. A tela ocupa o lugar da webcam durante o compartilhamento e não transmite o áudio do computador.
- Indicador de RTT e perda estimada de pacotes; clique nele para ver os detalhes por participante. Esses números não medem o atraso completo da voz.

As reuniões continuam limitadas a **8 pessoas**.

## Atualizações

Desde a versão 0.5, o aplicativo verifica novas versões ao abrir. Abra **Atualizações** (ou **Versões** desde a 0.6), baixe a versão disponível e, fora de uma chamada, escolha **Instalar e reiniciar**. O download é verificado por SHA-256 informado pelo GitHub; o executável anterior fica como backup. Versões 0.4 e anteriores precisam do primeiro download manual.

## Limites do protótipo

A conexão usa o serviço público gratuito de testes Mosquitto para sinalização e mensagens criptografadas, com histórico local. Esse serviço pode sofrer interrupções. Voz e vídeo usam conexão direta, sem servidor TURN; algumas redes e CGNAT podem impedir chamadas. A meta de 10 ms depende da rede e dos equipamentos e não é garantida.

Este repositório contém apenas downloads e documentação. O código-fonte permanece local. Não publique credenciais, backups, convites ou conversas nos relatos de problemas.
