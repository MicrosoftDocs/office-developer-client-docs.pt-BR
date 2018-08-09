---
title: Propriedade canônica PidTagOriginalAuthorSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorSearchKey
api_type:
- COM
ms.assetid: 4a10cf99-c5e6-4a24-b531-3aebb7800bfe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e5b283376d018b7b2675e05f994d586126437590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769544"
---
# <a name="pidtagoriginalauthorsearchkey-canonical-property"></a>Propriedade canônica PidTagOriginalAuthorSearchKey

  
  
**Aplica-se a**: Outlook 
  
Contém a chave de pesquisa do autor da primeira versão de uma mensagem, ou seja, a mensagem antes que está sendo encaminhada ou respondida.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORIGINAL_AUTHOR_SEARCH_KEY  <br/> |
|Identificador:  <br/> |0x0056  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Servidor  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é uma das propriedades de endereço para o autor de uma mensagem. No primeiro envio da mensagem, o aplicativo cliente deve definir essa propriedade como o valor da propriedade[PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md) **PR_SENDER_SEARCH_KEY**. Ele nunca é alterado quando a mensagem for encaminhada ou respondida. 
  
As propriedades de autor original permitem preservação de informações de fora do domínio de mensagens local. Quando uma mensagem é recebida de outro domínio de mensagens, como da Internet, essas propriedades fornecem uma maneira de garantir que as informações originais não sejam perdidas.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

