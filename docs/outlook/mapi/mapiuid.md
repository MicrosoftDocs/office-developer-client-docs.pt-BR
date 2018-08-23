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
ms.openlocfilehash: f7ec60768ab07c56969f538f196a1f9df5dbed17
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587163"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma versão independente da ordem de byte de uma estrutura [GUID](guid.md) é utilizada para identificar exclusivamente um provedor de serviços. 
  
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

 **AB**
  
> Uma matriz que contém um identificador de 16 bytes.
    
## <a name="remarks"></a>Comentários

Uma estrutura **MAPIUID** é uma estrutura **GUID** colocar em ordem de bytes de processador Intel®. 
  
MAPI cria **MAPIUID** estruturas de forma que torna muito rara para dois itens diferentes ter o mesmo identificador. Estruturas **MAPIUID** podem ser armazenadas como propriedades binárias ou como arquivos, sem relação com a ordem dos bytes do computador armazenando ou acessando as informações. 
  
 Estruturas **MAPIUID** são usadas: 
  
- Para identificar uma seção de perfil.
    
- Na entrada identificadores de mensagem armazenam em objetos de catálogo para identificar o provedor de serviços responsável de endereços.
    
- Na propriedade **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) das mensagens.
    
Para gerar um identificador **MAPIUID** por uma chave de pesquisa, provedores de serviços de chamarem [IMAPISupport::NewUID](imapisupport-newuid.md).
  
Quando um cliente transmite uma mensagem em uma rede, ele deve usar um formato de transmissão ou protocolo que não alterar a ordem de bytes de dados **MAPIUID** . 
  
Para obter mais informações sobre como as estruturas **MAPIUID** são usadas, consulte os tópicos a seguir: 
  
[Registrar identificadores exclusivos do provedor de serviços](registering-service-provider-unique-identifiers.md)
  
[Configurar um pedido de transporte](setting-transport-order.md)
  
## <a name="see-also"></a>Confira também



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[Estruturas MAPI](mapi-structures.md)

