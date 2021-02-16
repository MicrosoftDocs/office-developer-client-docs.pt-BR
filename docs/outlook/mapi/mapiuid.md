---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da314205f7d2dd746b72aa7e2b5ff2a13bb0c21b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432202"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma versão independente de ordem de byte de uma estrutura [GUID](guid.md) usada para identificar exclusivamente um provedor de serviços. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macro relacionada:  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>Members

 **ab**
  
> Uma matriz que contém um identificador de 16 byte.
    
## <a name="remarks"></a>Comentários

Uma **estrutura MAPIUID** é uma estrutura **GUID** colocada na ordem ® byte do processador Intel. 
  
MAPI creates **MAPIUID** structures in a way that makes it very rare for two different items to have the same identifier. **As estruturas MAPIUID** podem ser armazenadas como propriedades binárias ou como arquivos, sem considerar a ordenação de byte do computador que armazena ou acessa as informações. 
  
 **As estruturas MAPIUID** são usadas: 
  
- Para identificar uma seção de perfil.
    
- Nos identificadores de entrada do armazenamento de mensagens e dos objetos do livro de endereços para identificar o provedor de serviços responsável.
    
- Na **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) das mensagens.
    
Para gerar um **identificador MAPIUID** para uma chave de pesquisa, os provedores de serviços chamam [IMAPISupport::NewUID](imapisupport-newuid.md).
  
Quando um cliente transmite uma mensagem através de uma rede, ele deve usar um protocolo ou formato de transmissão que não altere a ordem de byte dos dados **MAPIUID.** 
  
Para obter mais informações sobre como as **estruturas MAPIUID** são usadas, consulte os seguintes tópicos: 
  
[Registrando identificadores exclusivos do provedor de serviços](registering-service-provider-unique-identifiers.md)
  
[Configurando a ordem de transporte](setting-transport-order.md)
  
## <a name="see-also"></a>Confira também



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[Estruturas MAPI](mapi-structures.md)

