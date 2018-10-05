---
title: PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382607"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>PidTagAddressBookHierarchicalRootDepartment

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Contém o nome diferenciado (DN) da autoridade raiz de catálogos de endereços hierárquicos (HAB). 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|Propriedade definida:  <br/> |Catálogo de Endereços  <br/> |
|ID de longo (LID):  <br/> |0x8C98  <br/> |
|Tipo de dados:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Catálogo de endereços do Exchange  <br/> |
   
## <a name="remarks"></a>Comentários

Esta é uma propriedade no contêiner endereços global (GAL) da lista e representa o nome diferenciado da raiz de endereços hierárquicos. Essa propriedade somente está presente no catálogo de endereços offline e nunca no serviços de domínio Active Directory (AD DS). Os chamadores devem passar MAPI_CACHE_ONLY para a chamada GetProps para evitar uma chamada de procedimento remoto. Se não estiver presente, os chamadores devem usar PR_EMS_AB_HAB_ROOT_DEPARTMENT, que é do tipo PT_OBJECT, para localizar o departamento de raiz. 
  
Depois que o departamento de raiz é obtido, ele pode ter um tipo de objeto MAPI_MAILUSER ou MAPI_DISTLIST. Se o tipo de objeto for MAPI_DISTLIST, o novo esquema é empregado. Se o tipo de objeto for MAPI_MAILUSER, o esquema anterior é empregado. 
  
- Microsoft Office Outlook 2007 Service Pack 2 oferece suporte a ambos os esquemas. 
    
- Microsoft Outlook 2010 e o Microsoft Outlook 2013 compatíveis com o novo esquema.
    
No novo esquema, todos os grupos departamentais também são listas de distribuição em são do tipo MAPI_DISTLIST. Membros de grupos departamentais e departamentos dentro dos grupos departamentais são obtidos por meio de PR_EMS_AB_MEMBER, exatamente como membros da lista de distribuição.
  
Depois que o departamento de raiz é obtido, ele pode ter um tipo de objeto MAPI_MAILUSER ou MAPI_DISTLIST. Se o tipo de objeto for MAPI_DISTLIST, o novo esquema está sendo usado. Se o tipo de objeto for MAPI_MAILUSER, o esquema antigo está sendo usado. 
  
No novo esquema, todos os grupos departamentais são também DLs em do tipo MAPI_DISTLIST.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Microsoft Exchange Server e as definições de conjunto de propriedades.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

