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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269920"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma versão independente de ordem de bytes de uma estrutura [GUID](guid.md) usada para identificar exclusivamente um provedor de serviços. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
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

Uma estrutura **MAPIUID** é uma estrutura **GUID** colocada na ordem de byte do processador Intel ®. 
  
O MAPI cria estruturas **MAPIUID** de uma maneira que torna muito raro que dois itens diferentes tenham o mesmo identificador. As estruturas **MAPIUID** podem ser armazenadas como propriedades binárias ou como arquivos, sem considerar a ordenação de bytes do computador que armazena ou acessa as informações. 
  
 As estruturas **MAPIUID** são usadas: 
  
- Para identificar uma seção de perfil.
    
- Nos identificadores de entrada dos objetos de repositório de mensagens e de catálogo de endereços para identificar o provedor de serviços responsável.
    
- Na propriedade **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de messages.
    
Para gerar um identificador de **MAPIUID** para uma chave de pesquisa, os provedores de serviços chamam [IMAPISupport:: NewUID](imapisupport-newuid.md).
  
Quando um cliente transmite uma mensagem através de uma rede, ele deve usar um formato de protocolo ou de transmissão que não altere a ordem de bytes dos dados de **MAPIUID** . 
  
Para obter mais informações sobre como as estruturas do **MAPIUID** são usadas, consulte os seguintes tópicos: 
  
[Registrando identificadores exclusivos do provedor de serviços](registering-service-provider-unique-identifiers.md)
  
[Configuração da ordem de transporte](setting-transport-order.md)
  
## <a name="see-also"></a>Confira também



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[Estruturas MAPI](mapi-structures.md)

