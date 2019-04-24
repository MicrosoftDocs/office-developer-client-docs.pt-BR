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
ms.openlocfilehash: b6abecc298df7a86afff9338752a15615c73b3a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348885"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois identificadores de entrada que pertencem a um determinado provedor de catálogo de endereços para determinar se eles se referem ao mesmo objeto de catálogo de endereços. 
  
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
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ . 
    
 _lpEntryID1_
  
> no Um ponteiro para o primeiro identificador de entrada a ser comparado.
    
 _cbEntryID2_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ . 
    
 _lpEntryID2_
  
> no Um ponteiro para o segundo identificador de entrada ser comparado.
    
 _ulFlags_
  
> no Serve deve ser zero.
    
 _lpulResult_
  
> bota Um ponteiro para o resultado da comparação. O conteúdo de _lpulResult_ é definido como true se os dois identificadores de entrada se referem ao mesmo objeto; caso contrário, o conteúdo será definido como FALSE. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Um ou ambos os identificadores de entrada passados com os parâmetros _lpEntryID1_ ou _lpEntryID2_ não são reconhecidos por qualquer provedor de catálogo de endereços. 
    
## <a name="remarks"></a>Comentários

Aplicativos cliente e provedores de serviços chamam o método **CompareEntryIDs** para comparar dois identificadores de entrada que pertencem a um único provedor de catálogo de endereços para determinar se eles se referem ao mesmo objeto. **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido. Essa situação pode ocorrer, por exemplo, após a instalação de uma nova versão de um provedor de catálogo de endereços. 
  
O MAPI passa essa chamada para o provedor de catálogo de endereços responsável pelos identificadores de entrada, determinando o provedor apropriado, combinando a estrutura [MAPIUID](mapiuid.md) nos identificadores de entrada com a estrutura **MAPIUID** registrada pelo provedor. 
  
Se os dois identificadores de entrada se referem ao mesmo objeto, **CompareEntryIDs** define o conteúdo do parâmetro _lpulResult_ como true; Se eles se referem a objetos diferentes, o **CompareEntryIDs** define o conteúdo como false. Em ambos os casos, **CompareEntryIDs** retorna S_OK. Se **CompareEntryIDs** retornar um erro, que pode ocorrer se nenhum provedor de catálogo de endereços tiver registrado uma estrutura **MAPIUID** que coincida com a do identificador de entrada, os clientes e provedores não deverão realizar nenhuma ação com base no resultado da diagrama. Em vez disso, eles devem adotar a abordagem mais conservadora para executar a ação. 
  
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

