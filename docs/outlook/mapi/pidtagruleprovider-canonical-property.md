---
title: Propriedade canônica PidTagRuleProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleProvider
api_type:
- COM
ms.assetid: 64f80a03-9ba4-495a-9666-b3a909335cb6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 19889a1f48a6088f0d5ad224f7e9189b112622fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280602"
---
# <a name="pidtagruleprovider-canonical-property"></a>Propriedade canônica PidTagRuleProvider

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome do aplicativo que define uma regra.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RULE_PROVIDER, PR_RULE_PROVIDER_A, PR_RULE_PROVIDER_W  <br/> |
|Identificador:  <br/> |0x6681  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Regras do lado do servidor  <br/> |
   
## <a name="remarks"></a>Comentários

Ações adiadas precisam dessas propriedades para identificar o código que deve interpretar e executar a ação de regra.
  
As regras armazenadas em caixas de correio e pastas são associadas ao aplicativo que as possui por uma cadeia de caracteres de provedor de regras. Um provedor de regras define e lida com regras em uma tabela de regras. Ele também fornece um meio de lidar com quaisquer ações adiadas se essas regras são definidas. Ações adiadas são criadas implicitamente pelo armazenamento de informações. Para mover ou copiar operações para um armazenamento diferente, se um provedor define uma regra de ação adiada, ele deve fornecer um manipulador para executar a ação quando a regra é acionada e uma ação adiada é criada.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Manipula mensagens de email de entrada em um servidor.
    
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

