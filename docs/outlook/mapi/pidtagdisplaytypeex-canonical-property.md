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
ms.openlocfilehash: 6eea30188543cb06545a9efad705f5593d4227a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360771"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>Propriedade canônica PidTagDisplayTypeEx

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o tipo de uma entrada, com relação a como a entrada deve ser exibida em uma linha de uma tabela para a lista de endereços global. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|Identificador:  <br/> |0x3905  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Catálogo de endereços MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade especifica o tipo de uma entrada, com relação a como deve ser exibida na lista de endereços global. Ele fornece informações adicionais que não podem ser representadas no **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
  
> [!NOTE]
> Os valores de **PR_DISPLAY_TYPE** e essa propriedade começam com "DT_" e são definidos em mapitags. h. Todos os valores não documentados são reservados para MAPI. Os aplicativos cliente não devem definir novos valores e devem estar preparados para lidar com um valor não documentado. 
  
Há algumas macros que podem ajudar a determinar os atributos de um objeto, como se ele é local, remoto ou controlado por segurança. Essas macros incluem: 
  
|**Macro**|**Valor**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0x80000000  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0x40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000ff00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000FF  <br/> |
|DTE_IS_REMOTE_VALID (v)  <br/> |(!! (v) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE (v)  <br/> |(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE (v)  <br/> |((v) &amp; DTE_MASK_REMOTE) \> \> 8)  <br/> |
|DTE_LOCAL (v)  <br/> |(v) &amp; DTE_MASK_LOCAL)  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |
   
Veja a seguir algumas observações sobre como usar essas macros. 
  
- Para verificar se uma entrada é uma entrada remota em outra floresta, aplique a macro DTE_IS_REMOTE_VALID ao valor dessa propriedade para verificar se o sinalizador DTE_FLAG_REMOTE_VALID está definido na entrada. Se for uma entrada remota, você poderá descobrir o tipo da entrada remota usando a macro DTE_REMOTE. 
    
- Nas configurações de floresta única e entre florestas, quando o **PR_DISPLAY_TYPE** tem o valor de DT_DISTLIST e DTE_IS_REMOTE_VALID é false, a aplicação da macro DTE_LOCAL ao valor dessa propriedade pode permitir que você identifique mais o tipo do objeto como DT_DISTLIST (uma lista de distribuição) ou DT_SEC_DISTLIST (uma lista de distribuição de segurança). 
    
- Se você aplicar a macro DTE_LOCAL ao valor de **PR_DISPLAY_TYPE_EX** e retornar o tipo DT_REMOTE_MAILUSER, a entrada será uma entrada remota. 
    
- Em uma única floresta ou em uma configuração entre florestas em que a replicação é controlada por uma lista de controle de acesso (ACL), você pode usar a macro DTE_IS_ACL_CAPABLE para determinar se uma entrada é uma entidade de segurança.
    
Em uma configuração entre florestas, **PR_DISPLAY_TYPE** tem o valor de DT_REMOTE_MAILUSER. A aplicação da macro DTE_REMOTE ao valor dessa propriedade pode permitir que você obtenha o tipo da entrada remota. Os possíveis tipos de entrada remota são os seguintes: 
  
|**Tipo de entrada remota**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0X00000003)  <br/> |Lista de distribuição dinâmica.  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0X00000001)  <br/> |Lista de distribuição.  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |Equipamento, por exemplo, uma impressora ou um projetor.  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |Usuário com uma caixa de correio.  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |Uma entrada da lista de endereços na lista de endereços global.  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |Sala de conferência.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |Lista de distribuição de segurança.  <br/> |
   
Em uma única floresta e em uma configuração entre florestas, quando **PR_DISPLAY_TYPE** tem o valor de DT_DISTLIST e DTE_IS_REMOTE_VALID é false, a aplicação da macro DTE_LOCAL ao valor dessa propriedade pode permitir que você obtenha o tipo da lista de distribuição . Os possíveis tipos de lista de distribuição são os seguintes: 
  
|**Tipo de lista de distribuição**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0X00000001)  <br/> |Lista de distribuição.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |Lista de distribuição de segurança.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

