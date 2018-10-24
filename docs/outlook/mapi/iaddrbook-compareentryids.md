---
title: IAddrBookCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBookCompareEntryIDs
api_type:
- COM
ms.assetid: 7dabc1d3-5ea4-482f-91a9-9ef3009eddd2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d6f983e49132e7ab6ea402a8e32bb5ec56d1efba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564847"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois identificadores de entrada que pertencem a um provedor de catálogo de endereço específico para determinar se eles se referem ao mesmo objeto de catálogo de endereços. 
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID1_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Um ponteiro para o primeiro identificador de entrada a ser comparada.
    
 _cbEntryID2_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Um ponteiro para o segundo identificador de entrada a ser comparada.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulResult_
  
> [out] Um ponteiro para o resultado da comparação. O conteúdo de _lpulResult_ estiverem definido como TRUE se os identificadores de dois entrada se referir ao mesmo objeto; Caso contrário, o conteúdo estiver definido como FALSE. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Um ou ambos os identificadores de entrada passados com os parâmetros _lpEntryID1_ ou _lpEntryID2_ não são reconhecidos pelas qualquer provedor de catálogo de endereços. 
    
## <a name="remarks"></a>Comentários

Aplicativos cliente e o serviço provedores chamada do método **CompareEntryIDs** para comparar os dois identificadores de entrada que pertence a um provedor de catálogo de endereço para determinar se eles se referem ao mesmo objeto. **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válida. Essa situação poderá ocorrer, por exemplo, depois que uma nova versão de um provedor de catálogo de endereços é instalada. 
  
MAPI passa essa chamada para o endereço provedor de catálogo que é responsável pelos identificadores de entrada, determinando o provedor apropriado combinando a estrutura [MAPIUID](mapiuid.md) em identificadores de entrada com a estrutura **MAPIUID** registrada pelo provedor. 
  
Se os identificadores de dois entrada se referir ao mesmo objeto, **CompareEntryIDs** define o conteúdo do parâmetro _lpulResult_ como TRUE; Se eles se referir a objetos diferentes, **CompareEntryIDs** define o conteúdo como FALSE. Em ambos os casos, **CompareEntryIDs** Retorna S_OK. Se **CompareEntryIDs** retornará um erro, que pode ocorrer se nenhum provedor de catálogo de endereços registrou uma estrutura **MAPIUID** que coincida com a pessoa nos identificadores de entrada, clientes e provedores não devem levar qualquer ação com base no resultado do comparação. Em vez disso, eles devem levar a abordagem mais conservadora à ação está sendo executada. 
  
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

