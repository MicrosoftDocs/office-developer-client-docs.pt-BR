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
ms.openlocfilehash: 03375a11be3f6f128db5f6147c5fbe901d0a0fa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766105"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**Aplica-se a**: Outlook 
  
Inicializa a um provedor de catálogo de endereços para a operação. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Implementada por:  <br/> |Provedores de catálogo de endereços  <br/> |
|Chamado pelo:  <br/> |MAPI  <br/> |
   
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
  
> [in] A instância de biblioteca de vínculo dinâmico do provedor de catálogo de endereços (DLL) que MAPI usado quando vinculado. 
    
 _lpMalloc_
  
> [in] Ponteiro para um objeto de alocador de memória expondo a interface OLE **IMalloc** . Talvez seja necessário usar esse método de alocação ao trabalhar com certas interfaces como **IStream**o provedor de catálogo de endereços. 
    
 _lpAllocateBuffer_
  
> [in] Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , que será usada onde exigidos pelo MAPI para alocar memória. 
    
 _lpAllocateMore_
  
> [in] Ponteiro para a função [MAPIAllocateMore](mapiallocatemore.md) , que será usada onde exigidos pelo MAPI para alocar memória adicional. 
    
 _lpFreeBuffer_
  
> [in] Ponteiro para a função de [MAPIFreeBuffer](mapifreebuffer.md) , para ser usada onde exigidos pelo MAPI para liberar memória. 
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores. O seguinte sinalizador pode ser definido:
    
MAPI_NT_SERVICE 
  
> O provedor está sendo carregado no contexto de um serviço do Windows, um tipo especial de processo sem acesso a qualquer interface do usuário. 
    
 _ulMAPIVer_
  
> [in] Número de versão da interface do provedor de serviço (SPI) que MAPI. Usa a DLL. Para o número da versão atual, consulte o MAPISPI. Arquivo de cabeçalho H. 
    
 _lpulProviderVer_
  
> [out] Ponteiro para o número de versão da SPI que usa esse provedor de catálogo de endereços. 
    
 _lppABProvider_
  
> [out] Ponteiro para um ponteiro para o objeto de provedor de catálogo de endereços inicializada.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores. 
    
MAPI_E_VERSION 
  
> A versão EDA sendo usada pelo MAPI não é compatível com o SPI sendo usado por este provedor.
    
## <a name="remarks"></a>Comentários

MAPI chama a função do ponto de entrada **ABProviderInit** ao inicializar um provedor de catálogo de endereços seguindo um logon do cliente. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Um provedor de catálogo de endereços deve implementar **ABProviderInit** como uma função de ponto de entrada na DLL do provedor. A implementação deve se basear no protótipo de função **ABPROVIDERINIT** , também especificado em MAPISPI. H. MAPI define **ABPROVIDERINIT** para usar o MAPI inicialização chamada tipo padrão, STDMAPIINITCALLTYPE, que faz com que o **ABProviderInit** a seguir a convenção de chamada CDECL. 
  
Um provedor pode ser inicializado várias vezes, como resultado que aparecem em vários perfis em uso simultâneo ou do que aparecem mais de uma vez no mesmo perfil. Porque o objeto de provedor contém contexto, **ABProviderInit** deve retornar um objeto de provedor diferente em _lppABProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo. 
  
O provedor de catálogo de endereços deve usar as funções apontadas pela _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria dos alocação de memória e desalocação. Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos do cliente, ao chamar interfaces de objeto, como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md). Se o provedor de espera-se também usar o alocador de memória OLE, ele deve chamar o método **AddRef** do objeto alocador apontado pelo parâmetro _lpMalloc_ . 
  
Para obter mais informações sobre como escrever **ABProviderInit**, consulte [Implementando uma função de ponto de entrada do endereço livro provedor](implementing-an-address-book-provider-entry-point-function.md). Para obter mais informações sobre as funções de ponto de entrada, consulte [Implementando uma função de ponto de entrada do serviço provedor](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Confira também

- [IABProvider : IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

