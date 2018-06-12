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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e1f15a5f031f5c5a9568b8a36722eaac011b814c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767771"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**Aplica-se a**: Outlook 
  
Define uma função de retorno de chamada que chamadas MAPI para ativar um controle de botão opcional em uma caixa de diálogo Catálogo de endereços. Normalmente, esse botão é um botão de **detalhes** . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Função definido implementada por:  <br/> |Provedores de serviços  <br/> |
|Função definido chamada pelo:  <br/> |MAPI  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulUIParam_
  
> [in] Alça das janelas de pai para todas as caixas de diálogo ou windows que exibe essa função.
    
 _lpvContext_
  
> [in] Ponteiro para um valor arbitrário passado para a função de retorno de chamada quando chamadas de MAPI-lo. Esse valor pode representar um endereço de significância ao aplicativo cliente. Geralmente, para código C++, _lpvContext_ representa um ponteiro para um objeto C++. 
    
 _cbEntryID_
  
> [in] Tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpSelection_ . 
    
 _lpSelection_
  
> [in] Ponteiro para o identificador de entrada definindo a seleção na caixa de diálogo.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Coment�rios

Aplicativos cliente chamam uma função de retorno de chamada com base em protótipo **LPFNBUTTON** para definir um botão em uma caixa de diálogo detalhes. O cliente passa um ponteiro para a função de retorno de chamada em chamadas para o método [IAddrBook::Details](iaddrbook-details.md) . 
  
Provedores de serviços de chamarem uma função de fora do gancho, com base em protótipo **LPFNBUTTON** para definir um botão em uma caixa de diálogo detalhes. O provedor passa um ponteiro para essa função gancho em chamadas para o método [IMAPISupport::Details](imapisupport-details.md) . 
  
Em ambos os casos, quando a caixa de diálogo é exibida e o usuário escolhe o botão definido, MAPI chama **LPFNBUTTON**. 
  
## <a name="see-also"></a>Confira também



[BuildDisplayTable](builddisplaytable.md)

