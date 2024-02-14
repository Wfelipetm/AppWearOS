Wear OS Audio Assistance App - Projeto DOMA
Este projeto consiste em um aplicativo desenvolvido pela empresa DOMA para dispositivos Wear OS, voltado para oferecer assistência para pessoas com deficiência visual. O aplicativo monitora as notificações do dispositivo e converte-as em áudio, proporcionando uma experiência de uso acessível e inclusiva.

Funcionalidades
Auxiliar de áudio
A classe AudioHelper fornece métodos para verificar a disponibilidade de saída de áudio e registrar callbacks para detectar dispositivos de áudio adicionados ou removidos. Principais funções:

audioOutputAvailable(int type): Verifica se a saída de áudio especificada está disponível no dispositivo.
registerAudioDeviceCallback(): Registra um callback para detectar dispositivos de áudio adicionados ou removidos.
Texto para fala
A classe TexttoSpeech é responsável por fornecer funcionalidades de conversão de texto para fala (Text-to-Speech, TTS). Principais funções:

speak(String text): Converte o texto especificado em áudio e reproduz em voz alta.
shutdown(): Interrompe a reprodução de áudio e libera recursos do TextToSpeech.
Serviço de Notificação
O serviço NotificationService estende a classe NotificationListenerService e é responsável por monitorar as notificações do dispositivo. Principais funções:

onNotificationPosted(StatusBarNotification sbn): Invocado quando uma nova notificação é postada. Converte o texto da notificação em áudio e reproduz em voz alta.
onNotificationRemoved(StatusBarNotification sbn): Invocado quando uma notificação é removida.
Atividade principal
A MainActivity é a atividade principal do aplicativo, onde a interface do usuário é exibida e as funcionalidades são utilizadas. Principais funcionalidades:

Inicia o serviço de escuta de notificações (NotificationService).
Verifica a disponibilidade de saída de áudio e atualiza a interface do usuário de acordo.
Fornece botão para abrir as configurações Bluetooth.
Utiliza o TexttoSpeech para falar mensagens para o usuário.
Instruções de Uso
Instale o aplicativo no seu dispositivo Wear OS.
Conceda as permissões necessárias, especialmente a permissão para acessar as notificações do dispositivo.
Ao receber notificações, o aplicativo as converterá em áudio e as reproduzirá em voz alta para o usuário.
Contribuições
Contribuições para o desenvolvimento e aprimoramento do aplicativo são bem-vindas. Sinta-se à vontade para enviar pull requests ou relatar problemas no repositório do projeto.


7 / 7





