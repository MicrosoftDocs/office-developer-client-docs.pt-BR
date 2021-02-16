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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326121"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>PidTagAddressBookHierarchicalRootDepartment

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Contém o nome diferenciado (DN) da raiz de endereço hierárquica (HAB). 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|Conjunto de propriedades:  <br/> |Catálogo de endereços  <br/> |
|Long ID (LID):  <br/> |0x8C98  <br/> |
|Tipo de dados:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Exchange Address Book  <br/> |
   
## <a name="remarks"></a>Comentários

Esta é uma propriedade no contêiner de lista de endereços global (GAL) e representa o nome diferenciado da raiz de endereço hierárquica. Essa propriedade só está presente no livro de endereços offline e nunca no Active Directory Domain Services (AD DS). Os chamadores devem passar MAPI_CACHE_ONLY chamada GetProps para evitar uma chamada de procedimento remoto. Se isso não estiver presente, os chamadores deverão usar PR_EMS_AB_HAB_ROOT_DEPARTMENT, que é do tipo PT_OBJECT, para encontrar o departamento raiz. 
  
Depois que o departamento raiz é obtido, ele pode ter um tipo de objeto MAPI_MAILUSER ou MAPI_DISTLIST. Se o tipo de objeto MAPI_DISTLIST, o novo esquema está sendo empregado. Se o tipo de objeto MAPI_MAILUSER, o esquema anterior está sendo empregado. 
  
- O Microsoft Office Outlook 2007 Service Pack 2 oferece suporte a ambos os esquemas. 
    
- O Microsoft Outlook 2010 e o Microsoft Outlook 2013 suportam o novo esquema.
    
No novo esquema, todos os grupos de departamentos também são listas de distribuição e são do tipo MAPI_DISTLIST. Membros de grupos de departamentos e departamentos dentro de grupos de departamentos são obtidos usando PR_EMS_AB_MEMBER, exatamente como membros da lista de distribuição.
  
Depois que o departamento raiz é obtido, ele pode ter um tipo de objeto MAPI_MAILUSER ou MAPI_DISTLIST. Se o tipo de objeto MAPI_DISTLIST, o novo esquema está sendo usado. Se o tipo de objeto MAPI_MAILUSER, o esquema antigo está sendo usado. 
  
No novo esquema, todos os grupos de departamentos também são DLs e são do tipo MAPI_DISTLIST.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo do Microsoft Exchange Server relacionadas.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

