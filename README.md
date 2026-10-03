# PulseVoice para Windows

Conversas privadas, chamadas de voz e vídeo e reuniões para até 8 pessoas. Aplicativo experimental para Windows 10/11 de 64 bits.

## Download

[Baixar PulseVoice.exe](https://github.com/OppressorLiber/pulsevoice-releases/releases/latest/download/PulseVoice.exe) · [Todas as versões](https://github.com/OppressorLiber/pulsevoice-releases/releases)

Abra o executável em uma pasta com permissão de escrita. Não precisa instalar Python.

## Conversas e perfil

Em **Perfil**, escolha foto, nome, descrição e status; copie seu convite e compartilhe com a pessoa que deseja adicionar. Depois de aceitar o contato, vocês podem trocar mensagens e iniciar uma chamada. Desde a versão 0.7, com ambos os aplicativos conectados, a outra pessoa recebe um aviso com som e **Atender / Recusar**. O convite também aparece no chat. Os avisos expiram em 60 segundos; **Não perturbar** recusa novas chamadas. O aplicativo precisa permanecer aberto para receber o aviso.

O histórico e a identidade ficam no computador. Mensagens pendentes são enviadas quando os dois contatos estiverem conectados. Exporte um backup protegido por senha em **Perfil** antes de trocar de computador. Não há recuperação por e-mail nem sincronização entre dispositivos.

## Reuniões

Em **Reuniões**, crie uma sala e compartilhe o convite. Dentro dela, **Dispositivos** permite escolher microfone, fones e webcam, incluindo **LumaCam Camera** quando a webcam virtual estiver ativa. O criador precisa permanecer conectado. Use fones para evitar eco.

A grade tem fotos, destaque de quem fala e participante fixado por duplo clique. Pelo painel do participante, ajuste o volume de 0 a 200% ou **Silenciar só para mim**. O indicador de RTT e perda estimada não mede o atraso completo da voz. As reuniões continuam limitadas a **8 pessoas**.

## Novidades da versão 0.8

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
