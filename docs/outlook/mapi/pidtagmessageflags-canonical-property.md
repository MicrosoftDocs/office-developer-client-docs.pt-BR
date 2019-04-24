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
ms.openlocfilehash: 5b660b592e77279a4d60f3a036724341352c9b6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325737"
---
# <a name="pidtagmessageflags-canonical-property"></a>Propriedade canônica PidTagMessageFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma bitmask de sinalizadores que indicam a origem e o estado atual de uma mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_FLAGS  <br/> |
|Identificador:  <br/> |0x0E07  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade é uma propriedade de mensagem não-transmittable exposta nas extremidades de envio e recebimento de uma transmissão, com valores diferentes dependendo do aplicativo cliente ou provedor de repositório envolvido. Essa propriedade é inicializada pelo provedor de armazenamento de mensagens ou cliente quando uma mensagem é criada e salva pela primeira vez e depois atualizada periodicamente pelo provedor de armazenamento de mensagens, por um provedor de transporte e pelo spooler de MAPI à medida que a mensagem é processada e seu estado alterações. 
  
Esta propriedade existe em uma mensagem antes e após o envio e em todas as cópias da mensagem recebida. Embora não seja uma propriedade de destinatário, ele é exposto de forma diferente para cada destinatário, de acordo com o fato de ter sido lido ou modificado por esse destinatário. 
  
Um ou mais dos seguintes sinalizadores podem ser definidos para esta propriedade:
  
MSGFLAG_ASSOCIATED 
  
> A mensagem é uma mensagem associada de uma pasta. O cliente ou provedor tem acesso somente leitura a esse sinalizador. O sinalizador MSGFLAG_READ é ignorado para mensagens associadas, que não retêm um estado de leitura/não leitura. 
    
MSGFLAG_FROMME 
  
> O envio do usuário de mensagens foi o usuário de mensagens que recebeu a mensagem. O cliente ou provedor tem acesso de leitura/gravação a este sinalizador até o primeiro [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) e somente leitura daí em diante. Este sinalizador deve ser definido pelo provedor de transporte. 
    
MSGFLAG_HASATTACH 
  
> A mensagem tem pelo menos um anexo. Este sinalizador corresponde à propriedade **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) da mensagem. O cliente tem acesso somente leitura a esse sinalizador. 
    
MSGFLAG_NRN_PENDING 
  
> Um relatório não lido precisa ser enviado para a mensagem. O cliente ou provedor tem acesso somente leitura a esse sinalizador. 
    
MSGFLAG_ORIGIN_INTERNET 
  
> A mensagem de entrada chegou pela Internet. Ele foi originado fora da organização ou de uma origem o gateway não pode considerar confiável. O cliente deve exibir uma mensagem apropriada para o usuário. Os provedores de transporte definem esse sinalizador; o cliente tem acesso somente leitura. 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> A mensagem de entrada chegou por um link externo diferente de X. 400 ou da Internet. Ele foi originado fora da organização ou de uma origem o gateway não pode considerar confiável. O cliente deve exibir uma mensagem apropriada para o usuário. Os provedores de transporte definem esse sinalizador; o cliente tem acesso somente leitura. 
    
MSGFLAG_ORIGIN_X400 
  
> A mensagem de entrada chegou por meio de um link X. 400. Ele foi originado fora da organização ou de uma origem o gateway não pode considerar confiável. O cliente deve exibir uma mensagem apropriada para o usuário. Os provedores de transporte definem esse sinalizador; o cliente tem acesso somente leitura. 
    
MSGFLAG_READ 
  
> A mensagem está marcada como tendo sido lida. Isso pode ocorrer como resultado de uma chamada a qualquer momento para [IMessage:: SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md). Os clientes também podem definir esse sinalizador chamando o método **IMAPIProp::** SetProps da mensagem antes de a mensagem ter sido salva pela primeira vez. Este sinalizador será ignorado se o sinalizador **MSGFLAG_ASSOCIATED** estiver definido. 
    
MSGFLAG_RESEND 
  
> A mensagem inclui uma solicitação para uma operação de reenvio com um relatório de não entrega. O cliente ou provedor tem acesso de leitura/gravação a este sinalizador até o primeiro [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) e somente leitura daí em diante. 
    
MSGFLAG_RN_PENDING 
  
> Um relatório de leitura precisa ser enviado para a mensagem. O cliente ou provedor tem acesso somente leitura a esse sinalizador. 
    
MSGFLAG_SUBMIT 
  
> A mensagem é marcada para envio como resultado de uma chamada para [IMessage:: SubmitMessage](imessage-submitmessage.md). Os provedores do repositório de mensagens definem esse sinalizador; o cliente tem acesso somente leitura. 
    
MSGFLAG_UNMODIFIED 
  
> A mensagem de saída não foi modificada desde a primeira vez que foi salva; a mensagem de entrada não foi modificada desde sua entrega. 
    
MSGFLAG_UNSENT 
  
> A mensagem ainda está sendo composta. Ele foi salvo, mas não foi enviado. O cliente ou provedor tem acesso de leitura/gravação a este sinalizador até o primeiro [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) e somente leitura daí em diante. Se um cliente não definir esse sinalizador quando a mensagem for enviada, o provedor de armazenamento de mensagens o definirá quando **IMessage:: SubmitMessage** for chamado. Normalmente, esse sinalizador é apagado após o envio da mensagem. 
    
Um provedor de armazenamento de mensagens ou cliente pode verificar o estado atual da mensagem a qualquer momento chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps para ler os valores de sinalizador. O cliente ou provedor também pode chamar o método [IMAPIProp::](imapiprop-setprops.md) SetProps para alterar quaisquer sinalizadores que atualmente têm acesso de leitura/gravação. 
  
Vários dos sinalizadores são sempre somente leitura. Alguns são de leitura/gravação até a primeira chamada para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) e, depois disso, se torna somente leitura no máximo **IMAPIProp::** SetProps está preocupado. Um desses, MSGFLAG_READ, pode ser alterado posteriormente através do [IMessage:: SetReadFlag](imessage-setreadflag.md) ou [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md). 
  
Os valores iniciais dessa propriedade normalmente são MSGFLAG_UNSENT e MSGFLAG_UNMODIFIED para indicar uma mensagem que ainda não foi enviada ou alterada. Quando uma mensagem é salva pela segunda vez, o provedor do repositório de mensagens limpa o sinalizador MSGFLAG_UNMODIFIED. Outro valor que um provedor de repositório de mensagens pode definir quando uma mensagem é salva é o sinalizador MSGFLAG_HASATTACH, indicando que a mensagem tem um ou mais anexos. A propriedade **PR_HASATTACH** é calculada a partir dessa configuração. 
  
Quando um cliente chama o método [IMessage:: SubmitMessage](imessage-submitmessage.md) para enviar a mensagem, o provedor do repositório de mensagens faz uma cópia dele para o spooler MAPI e atualiza essa propriedade definindo o sinalizador MSGFLAG_SUBMIT. O provedor de repositório de mensagens também define MSGFLAG_UNSENT se ainda não estiver definido. MSGFLAG_SUBMIT indica que o **SubmitMessage** foi chamado, iniciando o processo de envio e que a mensagem agora é somente leitura no cliente. MSGFLAG_UNSENT indica que o spooler MAPI está tratando a mensagem. Se o processo de envio for cancelado, o provedor do repositório de mensagens redefinirá esse sinalizador. 
  
Quando a mensagem é atribuída a um provedor de transporte para entrega, o provedor de transporte define o sinalizador MSGFLAG_FROMME se o remetente tivesse a mesma conta no servidor de mensagens à medida que a mensagem foi recebida. Os provedores de transporte definem MSGFLAG_FROMME para uma mensagem de entrada que foi enviada pelo usuário conectado no momento. Um cliente pode usar esse valor para determinar que é mais apropriado mostrar os nomes dos destinatários na tabela de conteúdo da pasta Itens enviados do que os nomes de remetente. As mensagens que foram salvas durante o processo de composição e que ainda não foram enviadas também devem ser exibidas com nomes de destinatários em vez de nomes de remetente. 
  
Para uma mensagem de entrada, um provedor de repositório de mensagens limpa o sinalizador MSGFLAG_READ para redefinir seu status de leitura. Um cliente pode definir ou limpar o sinalizador MSGFLAG_READ quando for necessário alterar o status de leitura e controlar o envio de relatórios de leitura e não leitura, chamando o método [IMessage:: SetReadFlag](imessage-setreadflag.md) da mensagem ou seus IMAPIFolder da pasta [: Método SetReadFlags](imapifolder-setreadflags.md) . A principal diferença entre esses métodos, além do objeto que os implementa, é que o método Folder pode afetar uma, várias ou todas as mensagens na pasta. O método Message afeta uma única mensagem. 
  
Um cliente também deve testar uma mensagem de entrada para os sinalizadores MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET e MSGFLAG_ORIGIN_MISC_EXT. Esses sinalizadores são definidos pelo provedor de transporte de entrada e indicam que a mensagem chegou de uma origem que o gateway não pode considerar confiável. Isso significa que a mensagem se originou fora da organização, ou internamente, mas de uma estação de trabalho não conhecida pelo Gateway. Em qualquer caso, a identidade do remetente pode não ser confirmada, e há um risco de introduzir um vírus de computador na organização. O cliente deve exibir uma mensagem de aviso para o usuário e oferecer uma opção de excluir a mensagem sem abri-la. 
  
Os provedores de repositório de mensagens definem o sinalizador MSGFLAG_UNMODIFIED para mensagens de entrada. MSGFLAG_UNMODIFIED Indica que uma mensagem não foi alterada desde a entrega. Um cliente não pode limpar esse valor após ele ter sido definido por um provedor de armazenamento de mensagens. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Manipula objetos Message e Attachment.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

