---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 804bd23a148b942fd4580d1e3465fc1f65ff5978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431509"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma função de retorno de chamada que MAPI chama para ativar um controle de botão opcional em uma caixa de diálogo do livro de endereços. Normalmente, esse botão é um **botão** Detalhes. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Função definida implementada por:  <br/> |Provedores de serviços  <br/> |
|Função definida chamada por:  <br/> |MAPI  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Alça das janelas pai para quaisquer caixas de diálogo ou janelas que essa função exibe.
    
 _lpvContext_
  
> [in] Ponteiro para um valor arbitrário passado para a função de retorno de chamada quando MAPI o chama. Esse valor pode representar um endereço significativo para o aplicativo cliente. Normalmente, para código C++,  _lpvContext_ representa um ponteiro para um objeto C++. 
    
 _cbEntryID_
  
> [in] Tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpSelection._ 
    
 _lpSelection_
  
> [in] Ponteiro para o identificador de entrada definindo a seleção na caixa de diálogo.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Os aplicativos cliente chamam uma função de retorno de chamada com base no protótipo **LPFNBUTTON** para definir um botão em uma caixa de diálogo de detalhes. O cliente passa um ponteiro para a função de retorno de chamada em chamadas para o [método IAddrBook::D etails.](iaddrbook-details.md) 
  
Os provedores de serviços chamam uma função de gancho com base no protótipo **LPFNBUTTON** para definir um botão em uma caixa de diálogo de detalhes. O provedor passa um ponteiro para essa função de gancho em chamadas para o [método IMAPISupport::D etails.](imapisupport-details.md) 
  
Em ambos os casos, quando a caixa de diálogo é exibida e o usuário escolhe o botão definido, MAPI chama **LPFNBUTTON**. 
  
## <a name="see-also"></a>Confira também



[BuildDisplayTable](builddisplaytable.md)

