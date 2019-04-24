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
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315383"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>Propriedade canônica PidLidValidFlagStringProof

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Valida se o valor da propriedade **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) foi definido por um agente que sabia o valor da propriedade **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidValidFlagStringProof  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085BF  <br/> |
|Tipo de dados:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Tarefa  <br/> |
   
## <a name="remarks"></a>Comentários

Em objetos que não podem ser enviados (objetos de email e de não-email), os clientes devem definir esse valor como o valor de **PR_MESSAGE_DELIVERY_TIME** ao modificar **dispidRequest**.
  
Como o valor de **PR_MESSAGE_DELIVERY_TIME** não pode ser previsto pelo remetente, se o valor dessa propriedade for igual ao valor de **PR_MESSAGE_DELIVERY_TIME**, é razoavelmente certo de que o valor de **dispidRequest** não seja proveniente do remetente da mensagem. Um cliente pode decidir como apresentar o valor de **dispidRequest** para o usuário final com base no resultado dessa comparação, de acordo com a política de segurança específica do cliente. Se o valor de **dispidRequest** for ignorado devido à presença de um valor de **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), essa propriedade deve ser ignorada.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica as propriedades e operações relacionadas à sinalização.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

