---
title: Propriedade canônica PidTagMessageFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageFlags
api_type:
- HeaderDef
ms.assetid: 7561112b-ca72-4c49-a8a0-cc1879a4e151
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f2e565dc8137edee441643a5d02a154f78737099
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769482"
---
# <a name="pidtagmessageflags-canonical-property"></a>Propriedade canônica PidTagMessageFlags

  
  
**Aplica-se a**: Outlook 
  
Contém uma bitmask dos sinalizadores que indicam a origem e o estado atual de uma mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_FLAGS  <br/> |
|Identificador:  <br/> |0x0E07  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é uma propriedade de mensagem nontransmittable exposta no nível o envio e recebimento extremidades de uma transmissão, com valores diferentes dependendo do aplicativo ou repositório provedor do cliente envolvido. Essa propriedade é inicializada, o provedor de armazenamento de cliente ou de mensagem quando uma mensagem é criada e salvo pela primeira vez e, em seguida, atualizada periodicamente o provedor de armazenamento de mensagem, um provedor de transporte e o MAPI spooler conforme a mensagem é processada e seu estado alterações. 
  
Essa propriedade existe em uma mensagem antes e após o envio e todas as cópias da mensagem recebida. Embora não seja uma propriedade de destinatário, ele é exposto forma diferente para cada destinatário de acordo com se ele tiver sido lidos ou modificado por que o destinatário. 
  
Um ou mais dos seguintes sinalizadores podem ser definido para essa propriedade:
  
MSGFLAG_ASSOCIATED 
  
> A mensagem é uma mensagem associada de uma pasta. O cliente ou o provedor tem acesso somente leitura para esse sinalizador. O sinalizador MSGFLAG_READ é ignorado para mensagens associadas, o qual não mantém um estado lido /. 
    
MSGFLAG_FROMME 
  
> O usuário enviando mensagens era o usuário mensagens recebendo a mensagem. O cliente ou o provedor tem acesso de leitura/gravação para esse sinalizador até a primeira chamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) e somente leitura depois disso. Esse sinalizador é destinado a ser definido pelo provedor de transporte. 
    
MSGFLAG_HASATTACH 
  
> A mensagem possui pelo menos um anexo. Esse sinalizador corresponde à propriedade de **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) da mensagem. O cliente tem acesso somente leitura para esse sinalizador. 
    
MSGFLAG_NRN_PENDING 
  
> Um relatório nonread precisa ser enviada para a mensagem. O cliente ou o provedor tem acesso somente leitura para esse sinalizador. 
    
MSGFLAG_ORIGIN_INTERNET 
  
> A mensagem de entrada foi recebida pela Internet. Ela se originou fora da organização ou de uma fonte que o gateway não pode considerar confiáveis. O cliente deve exibir uma mensagem apropriada para o usuário. Provedores de transporte definir esse sinalizador; o cliente tem acesso somente leitura. 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> A mensagem de entrada chegado por um link externo que não seja x. 400 ou a Internet. Ela se originou fora da organização ou de uma fonte que o gateway não pode considerar confiáveis. O cliente deve exibir uma mensagem apropriada para o usuário. Provedores de transporte definir esse sinalizador; o cliente tem acesso somente leitura. 
    
MSGFLAG_ORIGIN_X400 
  
> A mensagem de entrada foi recebida em um vínculo de x. 400. Ela se originou fora da organização ou de uma fonte que o gateway não pode considerar confiáveis. O cliente deve exibir uma mensagem apropriada para o usuário. Provedores de transporte definir esse sinalizador; o cliente tem acesso somente leitura. 
    
MSGFLAG_READ 
  
> A mensagem é marcada como tendo sido lidas. Isso pode ocorrer como resultado de uma chamada a qualquer momento para [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md). Os clientes também podem definir esse sinalizador chamando o método de **IMAPIProp::SetProps** da mensagem antes que a mensagem foi salvo pela primeira vez. Esse sinalizador é ignorada se o sinalizador **MSGFLAG_ASSOCIATED** está definido. 
    
MSGFLAG_RESEND 
  
> A mensagem inclui uma solicitação para uma operação de reenvio com um relatório de não entrega. O cliente ou o provedor tem acesso de leitura/gravação para esse sinalizador até a primeira chamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) e somente leitura depois disso. 
    
MSGFLAG_RN_PENDING 
  
> Um relatório de leitura precisa ser enviada para a mensagem. O cliente ou o provedor tem acesso somente leitura para esse sinalizador. 
    
MSGFLAG_SUBMIT 
  
> A mensagem é marcada para enviar como resultado de uma chamada para [IMessage::SubmitMessage](imessage-submitmessage.md). Provedores de armazenamento de mensagem definir esse sinalizador; o cliente tem acesso somente leitura. 
    
MSGFLAG_UNMODIFIED 
  
> A mensagem de saída não foi modificada desde na primeira vez que ela foi salva; a mensagem de entrada não foi modificada desde que ela foi entregue. 
    
MSGFLAG_UNSENT 
  
> A mensagem ainda está sendo composta. Ele é salvo, mas não foi enviado. O cliente ou o provedor tem acesso de leitura/gravação para esse sinalizador até a primeira chamada [IMAPIProp::SaveChanges](imapiprop-savechanges.md) e somente leitura depois disso. Se um cliente não definir esse sinalizador no momento em que a mensagem é enviada, o provedor de armazenamento de mensagens a define quando **IMessage::SubmitMessage** é chamado. Normalmente, esse sinalizador é limpa depois que a mensagem é enviada. 
    
Um provedor de armazenamento do cliente ou mensagem pode verificar o estado atual da mensagem a qualquer momento chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) para ler os valores de sinalizador. O cliente ou o provedor também pode chamar o método [IMAPIProp::SetProps](imapiprop-setprops.md) para alterar qualquer sinalizadores que atualmente têm acesso de leitura/gravação. 
  
Vários dos sinalizadores são sempre somente leitura. Alguns são leitura/gravação até que a primeira chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) e depois disso serão somente leitura que diz respeito **IMAPIProp::SetProps** . Um dos seguintes procedimentos, MSGFLAG_READ, pode ser alterado posteriormente através de [IMessage::SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md). 
  
Os valores iniciais para essa propriedade normalmente são MSGFLAG_UNSENT e MSGFLAG_UNMODIFIED para indicar uma mensagem que ainda não foram enviada ou alterada. Quando uma mensagem é salva para a segunda vez, o provedor de armazenamento de mensagem limpa o sinalizador MSGFLAG_UNMODIFIED. Outro valor que um provedor de armazenamento de mensagem pode ser definidas quando uma mensagem é salvo é o sinalizador MSGFLAG_HASATTACH, indicando que a mensagem tem um ou mais anexos. A propriedade **PR_HASATTACH** é computada a partir dessa definição. 
  
Quando um cliente chama o método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar a mensagem, o provedor de armazenamento de mensagem faz uma cópia dele para o spooler MAPI e atualiza essa propriedade, definindo o sinalizador MSGFLAG_SUBMIT. O provedor de armazenamento de mensagem também define MSGFLAG_UNSENT se ainda não estiver definida. MSGFLAG_SUBMIT indica que **SubmitMessage** tiver sido chamado, iniciar o processo de envio, e que a mensagem agora é somente leitura para o cliente. MSGFLAG_UNSENT indica que o spooler MAPI está tratando a mensagem. Se o processo de envio for cancelado, o provedor de armazenamento de mensagem redefine esse sinalizador. 
  
Quando a mensagem é determinada a um provedor de transporte para entrega, o provedor de transporte define o sinalizador MSGFLAG_FROMME se o remetente tinha a mesma conta no servidor de mensagens, como a mensagem foi recebida em. Provedores de transporte definir MSGFLAG_FROMME para uma mensagem de entrada que foi enviada pelo usuário conectado no momento. Um cliente pode usar esse valor para determinar o que é mais apropriado mostrar os nomes dos destinatários na tabela de conteúdo da pasta Itens enviados do que os nomes de remetente. Mensagens que foram salvas durante o processo de composição e ainda não enviadas também devem ser exibidas com os nomes dos destinatários em vez de nomes de remetente. 
  
Uma mensagem de entrada, um provedor de armazenamento de mensagem limpa o sinalizador MSGFLAG_READ para redefinir o seu status de leitura. Um cliente pode definir ou limpar o sinalizador MSGFLAG_READ quando for necessário alterar o status de leitura e controlar o envio de relatórios de leitura e nonread, chamando o método de [IMessage::SetReadFlag](imessage-setreadflag.md) da mensagem ou sua pasta [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) método. A principal diferença entre esses métodos, que não seja o objeto implementá-las, é que o método da pasta pode afetar uma, várias ou todas as mensagens na pasta. O método de mensagem afeta a uma única mensagem. 
  
Um cliente também deve testar uma mensagem de entrada para os sinalizadores MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET e MSGFLAG_ORIGIN_MISC_EXT. Esses sinalizadores estão definidos pelo provedor de transporte de entrada e indicam que a mensagem foi recebida de uma fonte que o gateway não pode ser considerados confiáveis. Isso significa que a mensagem se originou seja fora da organização, ou internamente mas a partir de uma estação de trabalho não conhecido para o gateway. Em qualquer caso, a identidade do remetente não pode ser confirmada e há um risco de introduzir um vírus na organização. O cliente deve exibir uma mensagem de aviso ao usuário e oferecem uma opção de excluir a mensagem sem abri-lo. 
  
Provedores de armazenamento de mensagem defina o sinalizador MSGFLAG_UNMODIFIED para mensagens de entrada. MSGFLAG_UNMODIFIED indica que uma mensagem não foi alterada desde a entrega. Um cliente não pode desmarcar esse valor depois que ele tiver sido definido por um provedor de armazenamento de mensagem. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

