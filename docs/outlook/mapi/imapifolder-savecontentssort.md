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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7c8ccada96b3e34372d488e16c85627e8b6b0cd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766984"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**Aplica-se a**: Outlook 
  
Define a ordem de classificação padrão para a tabela de conteúdo de uma pasta.
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _lpSortCriteria_
  
> [in] Um ponteiro para uma estrutura [SSortOrderSet](ssortorderset.md) que contém a ordem de classificação padrão. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a ordem de classificação padrão é definida. O seguinte sinalizador pode ser definido:
    
RECURSIVE_SORT 
  
> O conjunto de ordem de classificação padrão se aplica à pasta indicada e todas as suas subpastas.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A ordem de classificação for salva com êxito.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de armazenamento de mensagem não suporta a salvando uma ordem de classificação para suas tabelas de conteúdo de pasta.
    
## <a name="remarks"></a>Coment�rios

O método **IMAPIFolder::SaveContentsSort** estabelece uma ordem de classificação padrão para a tabela de conteúdo de uma pasta. Ou seja, quando um cliente chama o método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da pasta após o código chama **SaveContentsSort**, as linhas da tabela de conteúdo retornado aparecerá na ordem estabelecida pelo **SaveContentsSort**.
  
Nem todos os provedores de armazenamento de mensagem suportam **SaveContentsSort**; é aceitável para provedores de armazenamento de mensagem retornar MAPI_E_NO_SUPPORT do método **SaveContentsSort** . 
  
## <a name="see-also"></a>Confira também



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)

