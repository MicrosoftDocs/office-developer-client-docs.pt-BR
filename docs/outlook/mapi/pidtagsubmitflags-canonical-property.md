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
ms.openlocfilehash: ca31aece48236227a03d8e2114f8af4b127b8f90
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339351"
---
# <a name="pidtagsubmitflags-canonical-property"></a>Propriedade canônica PidTagSubmitFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma máscara de bits de sinalizadores indicando detalhes sobre um envio de mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SUBMIT_FLAGS  <br/> |
|Identificador:  <br/> |0x0E14  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI não transmitível  <br/> |
   
## <a name="remarks"></a>Comentários

Um ou mais dos sinalizadores a seguir podem ser definidos para a **PR_SUBMIT_FLAGS** bitmask: 
  
SUBMITFLAG_LOCKED 
  
> No momento, o spooler MAPI tem a mensagem bloqueada. 
    
SUBMITFLAG_PREPROCESS 
  
> A mensagem precisa de pré-processamento. Quando o spooler MAPI for feito o pré-processamento dessa mensagem, ele deverá chamar o método [IMessage::SubmitMessage.](imessage-submitmessage.md) O provedor de armazenamento de mensagens reconhece que o spooler, em vez do aplicativo cliente, chamou **SubmitMessage**, limpa o sinalizador e continua o envio de mensagens.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMsgStore::SetLockState](imsgstore-setlockstate.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

