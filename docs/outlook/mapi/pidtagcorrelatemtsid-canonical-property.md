---
title: Propriedade canônica PidTagCorrelateMtsid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagCorrelateMtsid
api_type:
- HeaderDef
ms.assetid: d0fc4e91-ed90-4d27-bd23-f01e99728e2d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96bfc184752b6a3e15434ad67ac8c2b4b26cac4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359931"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>Propriedade canônica PidTagCorrelateMtsid

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o identificador MTS (sistema de transferência de mensagens) usado na correlação de relatórios com mensagens enviadas.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CORRELATE_MTSID  <br/> |
|Identificador:  <br/> |0x0E0D  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentários

Quando um provedor de transporte encontra uma mensagem enviada com essa propriedade definida como TRUE, ela define essa propriedade como o identificador MTS para essa mensagem. Após a transmissão, essa propriedade é armazenada com a mensagem na pasta Itens enviados da mensagem de interpessoa (IPM).
  
Os sistemas de mensagens que dão suporte à correlação pelo identificador MTS, como X. 400, retêm o identificador como parte do envelope de transporte da mensagem original e também de quaisquer relatórios gerados em resposta a ele. Quando um relatório é entregue a partir de um sistema de mensagens, o provedor de transporte define essa propriedade para o identificador MTS original do envelope de transporte do relatório. Essa propriedade é então armazenada com o relatório.
  
Um aplicativo cliente pode manter uma pasta de resultados de pesquisa de todas as mensagens com esta propriedade. Quando um relatório chega a uma mensagem, o cliente pode aplicar restrições à pasta Search-Results, localizar a versão original da mensagem e correlacionar as informações da mensagem original com as novas informações.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

