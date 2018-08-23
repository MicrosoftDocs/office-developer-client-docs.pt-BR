---
title: Propriedade canônica PidTagSubmitFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubmitFlags
api_type:
- COM
ms.assetid: 9ea1c029-d53c-4c28-b413-560083b6215a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fb048d622aaf3cfa97f380e21324749d7421603e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563685"
---
# <a name="pidtagsubmitflags-canonical-property"></a>Propriedade canônica PidTagSubmitFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma bitmask dos sinalizadores indicando detalhes sobre o envio de uma mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SUBMIT_FLAGS  <br/> |
|Identificador:  <br/> |0x0E14  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI não transmittable  <br/> |
   
## <a name="remarks"></a>Comentários

Um ou mais dos seguintes sinalizadores podem ser definidas para o bitmask **PR_SUBMIT_FLAGS** : 
  
SUBMITFLAG_LOCKED 
  
> O MAPI spooler atualmente tem a mensagem protegida. 
    
SUBMITFLAG_PREPROCESS 
  
> A mensagem precisa pré-processamento. Quando terminar do MAPI spooler pré-processamento essa mensagem, ele deve chamar o método [IMessage::SubmitMessage](imessage-submitmessage.md) . O provedor de armazenamento de mensagem reconhece que o spooler, em vez do aplicativo cliente, tenha chamado **SubmitMessage**, limpa o sinalizador e continua o envio de mensagem.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

