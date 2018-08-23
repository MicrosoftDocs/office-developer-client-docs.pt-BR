---
title: Propriedade canônica PidTagDisplayTypeEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 30482f7d6acef7377a1b63bc3de4e43be48d8608
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583355"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>Propriedade canônica PidTagDisplayTypeEx

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o tipo de uma entrada, com relação a entrada como deve ser exibida em uma linha em uma tabela para a lista de endereços Global. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|Identificador:  <br/> |0x3905  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Catálogo de endereços MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade especifica o tipo de uma entrada, com relação a como ele deve ser exibido na lista de endereços Global. Ele fornece informações adicionais que não podem ser representadas em **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
  
> [!NOTE]
> Os valores de **PR_DISPLAY_TYPE** e essa propriedade começam com "DT_" e definidos no Mapitags.h. Todos os valores não documentados são reservados para MAPI. Aplicativos cliente não devem definir qualquer novos valores e devem estar preparados para lidar com um valor não documentado. 
  
Há algumas macros que podem ajudar a determinar os atributos de um objeto como se ele está local, remoto ou segurança controlada. Estas macros incluem: 
  
|**Macro**|**Valor**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0x80000000)  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0x40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000ff00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000ff  <br/> |
|DTE_IS_REMOTE_VALID(v)  <br/> |(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE(v)  <br/> |(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE(v)  <br/> |(((v) &amp; DTE_MASK_REMOTE) \> \> 8)  <br/> |
|DTE_LOCAL(v)  <br/> |((v) &amp; DTE_MASK_LOCAL)  <br/> |
|DT_ROOM  <br/> |((ULONG) 0X00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0X00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0X00000009)  <br/> |
   
A seguir estão algumas observações sobre como usar essas macros. 
  
- Para verificar se uma entrada é uma entrada remota em outra floresta, se aplicam a macro DTE_IS_REMOTE_VALID com o valor dessa propriedade para verificar se o sinalizador DTE_FLAG_REMOTE_VALID está definido na entrada. Se for uma entrada remota, você pode então descobrir o tipo da entrada remoto usando a macro DTE_REMOTE. 
    
- Em configurações de floresta única e entre florestas, quando **PR_DISPLAY_TYPE** tem o valor de DT_DISTLIST e DTE_IS_REMOTE_VALID for false, a aplicação de macro DTE_LOCAL com o valor dessa propriedade pode permitem que você identifique ainda mais o tipo do objeto como DT_DISTLIST (uma lista de distribuição) ou DT_SEC_DISTLIST (uma lista de distribuição de segurança). 
    
- Se você aplicar a macro DTE_LOCAL como o valor de **PR_DISPLAY_TYPE_EX** e retorna o tipo DT_REMOTE_MAILUSER, a entrada é uma entrada remota. 
    
- Em uma única floresta ou em uma configuração entre florestas onde a replicação é controlada por uma lista de controle de acesso (ACL), você pode usar a macro DTE_IS_ACL_CAPABLE para determinar se uma entrada é uma entidade de segurança.
    
Em uma configuração entre florestas, **PR_DISPLAY_TYPE** tem o valor de DT_REMOTE_MAILUSER. A aplicação de macro DTE_REMOTE com o valor dessa propriedade pode permitem que você obtenha o tipo da entrada remoto. Os tipos possíveis de entrada remota são as seguintes: 
  
|**Tipo de entrada remoto**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0X00000003)  <br/> |Lista de distribuição dinâmica.  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0X00000001)  <br/> |Lista de distribuição.  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0X00000008)  <br/> |Equipamento, por exemplo, uma impressora ou em um projetor.  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0X00000000)  <br/> |Usuário com uma caixa de correio.  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0X00000000)  <br/> |Uma entrada da lista de endereços na lista de endereços Global.  <br/> |
|DT_ROOM  <br/> |((ULONG) 0X00000007)  <br/> |Sala de conferência.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0X00000009)  <br/> |Lista de distribuição de segurança.  <br/> |
   
Em ambos os uma única floresta e em uma entre florestas configuração, quando **PR_DISPLAY_TYPE** tem o valor de DT_DISTLIST e DTE_IS_REMOTE_VALID for false, a aplicação de macro DTE_LOCAL com o valor dessa propriedade pode permitem que você obtenha o tipo da lista de distribuição . Os possíveis tipos de lista de distribuição são as seguintes: 
  
|**Tipo de lista de distribuição**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0X00000001)  <br/> |Lista de distribuição.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0X00000009)  <br/> |Lista de distribuição de segurança.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
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

