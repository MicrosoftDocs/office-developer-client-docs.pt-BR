---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c142424bb050ae287f54a87ea8a5e0ea45acb12c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351202"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define a ordem de classificação padrão para a tabela de conteúdo de uma pasta.
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpSortCriteria_
  
> no Um ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que contém a ordem de classificação padrão. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como a ordem de classificação padrão é definida. O seguinte sinalizador pode ser definido:
    
RECURSIVE_SORT 
  
> O conjunto de ordem de classificação padrão se aplica à pasta indicada e a todas as suas subpastas.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A ordem de classificação foi salva com êxito.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de repositório de mensagens não oferece suporte para salvar uma ordem de classificação para suas tabelas de conteúdo da pasta.
    
## <a name="remarks"></a>Comentários

O método **IMAPIFolder:: SaveContentsSort** estabelece uma ordem de classificação padrão para a tabela de conteúdo de uma pasta. Ou seja, quando um cliente chama o método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable da pasta após o código chamar **SaveContentsSort**, as linhas na tabela de conteúdo retornada aparecerão na ordem estabelecida por **SaveContentsSort**.
  
Nem todos os provedores de repositório de mensagens dão suporte a **SaveContentsSort**; é aceitável que os provedores de repositórios de mensagens retornem MAPI_E_NO_SUPPORT do método **SaveContentsSort** . 
  
## <a name="see-also"></a>Confira também



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

