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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424256"
---
# <a name="iaddrbookcompareentryids"></a>IAddrBook::CompareEntryIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois identificadores de entrada que pertencem a um provedor de agendas específica para determinar se eles se referem ao mesmo objeto do livro de endereços. 
  
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
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Um ponteiro para o identificador da primeira entrada a ser comparado.
    
 _cbEntryID2_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Um ponteiro para o segundo identificador de entrada a ser comparado.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulResult_
  
> [out] Um ponteiro para o resultado da comparação. O conteúdo de  _lpulResult_ será definido como TRUE se os dois identificadores de entrada se referirem ao mesmo objeto; caso contrário, o conteúdo será definido como FALSE. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Um ou ambos os identificadores de entrada passados com os parâmetros  _lpEntryID1_ ou  _lpEntryID2_ não são reconhecidos por nenhum provedor de livro de endereços. 
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente e provedores de serviços chamam o método **CompareEntryIDs** para comparar dois identificadores de entrada que pertencem a um único provedor de agendamento de endereços para determinar se eles se referem ao mesmo objeto. **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido. Essa situação pode ocorrer, por exemplo, após a instalação de uma nova versão de um provedor de agendas. 
  
O MAPI passa essa chamada para o provedor de agendamento de endereços responsável pelos identificadores de entrada, determinando o provedor apropriado, correspondendo a estrutura [MAPIUID](mapiuid.md) nos identificadores de entrada com a estrutura **MAPIUID** registrada pelo provedor. 
  
Se os dois identificadores de entrada se referirem ao mesmo objeto, **CompareEntryIDs** define o conteúdo do parâmetro  _lpulResult_ como VERDADEIRO; se eles se referirem a objetos diferentes, **CompareEntryIDs** define o conteúdo como FALSE. Em ambos os casos, **CompareEntryIDs** retorna S_OK. Se **CompareEntryIDs** retornar um erro, que pode ocorrer se nenhum provedor de agendas tiver registrado uma estrutura **MAPIUID** que corresponde à dos identificadores de entrada, os clientes e provedores não devem tomar nenhuma ação com base no resultado da comparação. Em vez disso, eles devem tomar a abordagem mais conservador para a ação que está sendo executada. 
  
## <a name="see-also"></a>Confira também



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

