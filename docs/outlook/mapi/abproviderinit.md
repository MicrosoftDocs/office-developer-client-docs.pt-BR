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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428281"
---
# <a name="abproviderinit"></a>ABProviderInit
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicializa um provedor de agendas para operação. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Implementado por:  <br/> |Provedores de lista de endereços  <br/> |
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
  
> [in] A instância da biblioteca de vínculo dinâmico (DLL) do provedor de endereços que o MAPI usou ao vincular. 
    
 _lpMalloc_
  
> [in] Ponteiro para um objeto alocador de memória expondo a interface **IMalloc OLE.** O provedor de agendamento pode precisar usar esse método de alocação ao trabalhar com determinadas interfaces, como **IStream**. 
    
 _lpAllocateBuffer_
  
> [in] Ponteiro para a [função MAPIAllocateBuffer,](mapiallocatebuffer.md) a ser usado onde exigido por MAPI para alocar memória. 
    
 _lpAllocateMore_
  
> [in] Ponteiro para a [função MAPIAllocateMore,](mapiallocatemore.md) a ser usado onde exigido por MAPI para alocar memória adicional. 
    
 _lpFreeBuffer_
  
> [in] Ponteiro para a [função MAPIFreeBuffer,](mapifreebuffer.md) a ser usado onde exigido por MAPI para liberar memória. 
    
 _ulFlags_
  
> [in] Máscara de bits de sinalizadores. O sinalizador a seguir pode ser definido:
    
MAPI_NT_SERVICE 
  
> O provedor está sendo carregado no contexto de um serviço Windows, um tipo especial de processo sem acesso a qualquer interface do usuário. 
    
 _ulMAPIVer_
  
> [in] Número da versão da interface do provedor de serviços (SPI) que MAPI.DLL usa. Para o número da versão atual, consulte o MAPISPI. Arquivo de header H. 
    
 _lpulProviderVer_
  
> [out] Ponteiro para o número de versão do SPI que este provedor de agendas usa. 
    
 _lppABProvider_
  
> [out] Ponteiro para um ponteiro para o objeto de provedor de agenda de endereços inicializado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados. 
    
MAPI_E_VERSION 
  
> A versão SPI usada por MAPI não é compatível com o SPI usado por esse provedor.
    
## <a name="remarks"></a>Comentários

MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Um provedor de agendas deve implementar **ABProviderInit** como uma função de ponto de entrada na DLL do provedor. A implementação deve ser baseada no protótipo de **função ABPROVIDERINIT,** também especificado em MAPISPI.H. MAPI define **ABPROVIDERINIT** para usar o tipo de chamada de inicialização mapi padrão, STDMAPIINITCALLTYPE, que faz com que **ABProviderInit** siga a convenção de chamada CDECL. 
  
Um provedor pode ser inicializado várias vezes, como resultado de aparecer em vários perfis em uso simultâneo ou de aparecer mais de uma vez no mesmo perfil. Como o objeto do provedor contém contexto, **ABProviderInit** deve retornar um objeto de provedor diferente em  _lppABProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo. 
  
O provedor de agendamento deve usar as funções apontadas por  _lpAllocateBuffer_,  _lpAllocateMore_ e  _lpFreeBuffer_ para a maioria da alocação e alocação de memória. Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos cliente ao chamar interfaces de objeto como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md). Se o provedor também espera usar o alocador de memória OLE, ele deve chamar o método **IUnknown::AddRef** do objeto alocador apontado pelo parâmetro _lpMalloc._ 
  
For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md). Para obter mais informações sobre funções de ponto de entrada, consulte [Implementando uma função de](implementing-a-service-provider-entry-point-function.md)ponto de entrada do provedor de serviços. 
  
## <a name="see-also"></a>Confira também

- [IABProvider : IUnknown](iabprovideriunknown.md) 
- [MSProviderInit](msproviderinit.md)
- [XPProviderInit](xpproviderinit.md)

