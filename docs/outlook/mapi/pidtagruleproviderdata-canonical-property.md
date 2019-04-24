---
title: Propriedade canônica PidTagRuleProviderData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProviderData
api_type:
- COM
ms.assetid: b04a277c-b483-4f54-b360-311034b9a7ee
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e4d209c4f185ff253476beb04913e6a64884f9b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335417"
---
# <a name="pidtagruleproviderdata-canonical-property"></a>Propriedade canônica PidTagRuleProviderData

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma propriedade opaca que o cliente define para o uso exclusivo do cliente. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RULE_PROVIDER_DATA  <br/> |
|Identificador:  <br/> |0x6684  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Regras no servidor  <br/> |
   
## <a name="remarks"></a>Comentários

O servidor deve preservar o valor dessa propriedade se tiver sido definido pelo cliente, mas deve ignorar seu conteúdo durante a avaliação e o processamento da regra.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipula mensagens de email de entrada em um servidor.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas. 
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagRuleProvider](pidtagruleprovider-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

