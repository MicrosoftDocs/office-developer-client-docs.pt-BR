---
title: Propriedade canônica PidLidValidFlagStringProof
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: efbbffe184e965caae84db54383e1431dfb1a569
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585819"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>Propriedade canônica PidLidValidFlagStringProof

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida se o valor da propriedade **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) foi definido para um operador que sabia o valor da propriedade **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidValidFlagStringProof  <br/> |
|Propriedade definida:  <br/> |PSETID_Common  <br/> |
|ID de longo (LID):  <br/> |0x000085BF  <br/> |
|Tipo de dados:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentários

Nos objetos não possa ser enviado (email recebido e objetos não sejam de email), os clientes devem definir esse valor como o valor de **PR_MESSAGE_DELIVERY_TIME** ao modificar **dispidRequest**.
  
Como o valor da **PR_MESSAGE_DELIVERY_TIME** não pode ser previsto pelo remetente, se o valor dessa propriedade é igual ao valor de **PR_MESSAGE_DELIVERY_TIME**, ele é razoável certeza de que o valor da **dispidRequest** não especificou são originárias do remetente da mensagem. Um cliente pode decidir como o valor presente de **dispidRequest** para o usuário final com base no resultado desta comparação de acordo com a diretiva de segurança específica do cliente. Se o valor de **dispidRequest** será ignorado devido à presença de um valor para **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), esta propriedade deve ser ignorada.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas a sinalização.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

