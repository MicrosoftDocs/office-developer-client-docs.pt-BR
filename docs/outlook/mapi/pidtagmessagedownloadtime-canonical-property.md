---
title: Propriedade canônica PidTagMessageDownloadTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b47d104ade6a7d23f5630d15697b330360d027b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769472"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>Propriedade canônica PidTagMessageDownloadTime

  
  
**Aplica-se a**: Outlook 
  
Contém o tempo estimado para baixar uma mensagem de um servidor remoto para um armazenamento de mensagens local. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|Identificador:  <br/> |0x0E18  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é expresso em segundos e representa a melhor estimativa de tempo seria necessário um provedor de transporte remoto para baixar uma determinada mensagem de seu local atual para um armazenamento de mensagens local para o cliente de exibição da pasta do cabeçalho. Normalmente, o provedor de transporte remoto calcula o valor dessa propriedade dividindo-se o valor da propriedade **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) pela velocidade do link communications em bytes por segundo. Se o provedor não pode calcular o tempo de download, por exemplo, se não souber a velocidade de link, ele deve fornecer um valor **PT_ERROR** como **MAPI_E_NO_SUPPORT** para esta coluna na tabela de conteúdo de pasta de cabeçalho. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

