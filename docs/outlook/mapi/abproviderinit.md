---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: acec07df0b72685cf9ec6b21499c730b72f58c59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328109"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicializa um provedor de catálogo de endereços para operação. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi. h  <br/> |
|Implementado por:  <br/> |Provedores de catálogo de endereços  <br/> |
|Chamado por:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT ABProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPABPROVIDER FAR * lppABProvider
);
```

## <a name="parameters"></a>Parâmetros

 _hInstance_
  
> no A instância da biblioteca de vínculo dinâmico (DLL) do provedor do catálogo de endereços que o MAPI usou quando se vinculou. 
    
 _lpMalloc_
  
> no Ponteiro para um objeto de alocador de memória expondo a interface **IMalloc** do OLE. O provedor de catálogo de endereços pode precisar usar esse método de alocação ao trabalhar com determinadas interfaces, como **IStream**. 
    
 _lpAllocateBuffer_
  
> no Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , a ser usado onde o MAPI deve alocar memória. 
    
 _lpAllocateMore_
  
> no Ponteiro para a função [MAPIAllocateMore](mapiallocatemore.md) , a ser usado, onde o MAPI deve alocar memória adicional. 
    
 _lpFreeBuffer_
  
> no Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , a ser usado onde o MAPI deve liberar memória. 
    
 _ulFlags_
  
> no Bitmask de sinalizadores. O seguinte sinalizador pode ser definido:
    
MAPI_NT_SERVICE 
  
> O provedor está sendo carregado no contexto de um serviço do Windows, um tipo especial de processo sem acesso a qualquer interface do usuário. 
    
 _ulMAPIVer_
  
> no Número da versão da interface do provedor de serviços (SPI) que o MAPI. DLL usa. Para o número da versão atual, consulte o MAPISPI. Arquivo de cabeçalho H. 
    
 _lpulProviderVer_
  
> bota Ponteiro para o número da versão do SPI que este provedor de catálogo de endereços usa. 
    
 _lppABProvider_
  
> bota Ponteiro para um ponteiro para o objeto do provedor de catálogo de endereços inicializado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados. 
    
MAPI_E_VERSION 
  
> A versão SPI que está sendo usada pelo MAPI não é compatível com o SPI que está sendo usado por este provedor.
    
## <a name="remarks"></a>Comentários

MAPI chama a função de ponto de entrada **ABProviderInit** para inicializar um provedor de catálogo de endereços após um logon do cliente. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Um provedor de catálogo de endereços deve implementar **ABProviderInit** como uma função de ponto de entrada na DLL do provedor. A implementação deve ser baseada no protótipo de função **ABPROVIDERINIT** , também especificado em MAPISPI. 0. MAPI define **ABPROVIDERINIT** para usar o tipo de chamada de inicialização MAPI padrão, STDMAPIINITCALLTYPE, que faz com que o **ABPROVIDERINIT** siga a Convenção de chamada do cdecl. 
  
Um provedor pode ser inicializado várias vezes, como resultado da apresentação de vários perfis em uso simultâneo ou de ser exibido mais de uma vez no mesmo perfil. Como o objeto Provider contém contexto, **ABProviderInit** deve retornar um objeto Provider diferente no _lppABProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo. 
  
O provedor de catálogo de endereços deve usar as funções apontadas por _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maior parte da alocação de memória e desalocação. Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos cliente ao chamar interfaces de objeto, como [IMAPIProp::](imapiprop-getprops.md) GetProps e IMAPITable [:: QueryRows](imapitable-queryrows.md). Se o provedor também espera usar o alocador de memória OLE, ele deve chamar o método **IUnknown:: AddRef** do objeto de alocador apontado pelo parâmetro _lpMalloc_ . 
  
Para saber mais sobre como escrever **ABProviderInit**, confira [a implementação de uma função de ponto de entrada do provedor de catálogo de endereços](implementing-an-address-book-provider-entry-point-function.md). Para obter mais informações sobre funções de ponto de entrada, consulte [implementando uma função de ponto de entrada do provedor de serviços](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Confira também

- [IABProvider : IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

