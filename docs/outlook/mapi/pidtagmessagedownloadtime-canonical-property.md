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
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407925"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a>Propriedade canônica PidTagMessageDownloadTime

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o tempo estimado para baixar uma mensagem de um servidor remoto para um armazenamento de mensagens local. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_DOWNLOAD_TIME  <br/> |
|Identificador:  <br/> |0x0E18  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é expressa em segundos e representa a melhor estimativa do tempo que um provedor de transporte remoto levará para baixar uma determinada mensagem de seu local atual para um local de armazenamento de mensagens para o cliente que está exibindo a pasta de controle. O provedor de transporte remoto normalmente calcula o valor dessa propriedade dividindo o valor da propriedade **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) pela velocidade do link de comunicação em bytes por segundo. Se o provedor não puder calcular o tempo de download, por exemplo, se não sabe **a** velocidade do link, ele deverá fornecer um valor de PT_ERROR como **MAPI_E_NO_SUPPORT** para essa coluna na tabela de conteúdo da pasta de título. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

