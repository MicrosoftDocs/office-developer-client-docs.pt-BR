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
ms.openlocfilehash: 468cda97398bc393b1c0a65e2c13df5ba3ade3aa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568907"
---
# <a name="pidtagcorrelatemtsid-canonical-property"></a>Propriedade canônica PidTagCorrelateMtsid

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o identificador de sistema (MTS) de transferência de mensagem usado na correlação relatórios com as mensagens enviadas.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CORRELATE_MTSID  <br/> |
|Identificador:  <br/> |0x0E0D  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentários

Quando um provedor de transporte encontra uma mensagem enviada com esta propriedade é definida como TRUE, ele define essa propriedade para o identificador de MTS para essa mensagem. Após a transmissão, essa propriedade é armazenada com a mensagem na pasta Itens enviados interpessoais mensagens (IPM).
  
Sistemas de mensagens que oferecem suporte a correlação pelo identificador MTS, como x. 400, retêm o identificador como parte do envelope transporte da mensagem original e também de quaisquer relatórios gerados em resposta a ele. Quando um relatório é entregue de tal um sistema de mensagens, o provedor de transporte define essa propriedade para o identificador de MTS original do envelope de transporte do relatório. Em seguida, essa propriedade é armazenada com o relatório.
  
Um aplicativo cliente pode manter uma pasta de resultados de pesquisa de todas as mensagens que têm essa propriedade. Quando um relatório entra dessa mensagem, o cliente pode aplicar restrições para a pasta de resultados de pesquisa, encontre a versão original da mensagem e correlacionar informações da mensagem original com as novas informações.
  
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

