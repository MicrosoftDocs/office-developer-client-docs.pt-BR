---
title: XPProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.XPProviderInit
api_type:
- COM
ms.assetid: df6eacf4-1cf9-4c25-806f-f87c38dad597
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428533"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicializa um provedor de transporte para operação.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Implementado por:  <br/> |Provedores de transporte  <br/> |
|Chamado por:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT XPProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPXPPROVIDER FAR * lppXPProvider
);
```

## <a name="parameters"></a>Parâmetros

 _hInstance_
  
> [in] A instância da biblioteca de vínculo dinâmico (DLL) do provedor de transporte que o MAPI usou ao carregar a DLL.
    
 _lpMalloc_
  
> [in] Ponteiro para um objeto alocador de memória expondo a interface **IMalloc OLE.** O provedor de transporte pode precisar usar esse método de alocação ao trabalhar com determinadas interfaces, como **IStream**. 
    
 _lpAllocateBuffer_
  
> [in] Ponteiro para a [função MAPIAllocateBuffer,](mapiallocatebuffer.md) a ser usado para alocar memória. 
    
 _lpAllocateMore_
  
> [in] Ponteiro para a [função MAPIAllocateMore,](mapiallocatemore.md) a ser usado para alocar memória adicional. 
    
 _lpFreeBuffer_
  
> [in] Ponteiro para a [função MAPIFreeBuffer,](mapifreebuffer.md) a ser usado para liberar memória. 
    
 _ulFlags_
  
> [in] Máscara de bits de sinalizadores. O sinalizador a seguir pode ser definido:
    
MAPI_NT_SERVICE 
  
> O provedor está sendo carregado no contexto de um serviço Windows, um tipo especial de processo sem acesso a qualquer interface do usuário. 
    
 _ulMAPIVer_
  
> [in] Número da versão da interface do provedor de serviços (SPI) que Mapi.dll usa. Para o número da versão atual, consulte o arquivo de header Mapispi.h. 
    
 _lpulProviderVer_
  
> [out] Ponteiro para o número de versão do SPI que este provedor de transporte usa. 
    
 _lppXPProvider_
  
> [out] Ponteiro para um ponteiro para o objeto de provedor de transporte inicializado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados. 
    
MAPI_E_VERSION 
  
> A versão SPI usada por MAPI não é compatível com o SPI usado por esse provedor.
    
## <a name="remarks"></a>Comentários

O MAPI chama a função de ponto de entrada **XPProviderInit** para inicializar um provedor de transporte após um logon do cliente. **XPProviderInit** é chamado uma vez para cada provedor de transporte especificado no perfil do cliente. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Um provedor de transporte deve implementar **XPProviderInit** como uma função de ponto de entrada na DLL do provedor. A implementação deve ser baseada no protótipo da **função XPPROVIDERINIT,** também especificado em Mapispi.h. MAPI define **XPPROVIDERINIT** para usar o tipo de chamada de inicialização mapi padrão, STDMAPIINITCALLTYPE, que faz com que **XPProviderInit** siga a convenção de chamada CDECL. Uma vantagem do CDECL é que as chamadas podem ser tentadas mesmo se o número de parâmetros de chamada não corresponder ao número de parâmetros definidos. 
  
Um provedor pode ser inicializado várias vezes como resultado de aparecer em vários perfis em uso simultâneo ou de aparecer mais de uma vez no mesmo perfil. Como o objeto do provedor contém contexto, **XPProviderInit** deve retornar um objeto de provedor diferente em  _lppXPProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo. 
  
O provedor de transporte deve usar as funções apontadas por  _lpAllocateBuffer_,  _lpAllocateMore_ e  _lpFreeBuffer_ para a maioria da alocação e alocação de memória. Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos cliente ao chamar interfaces de objeto como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md). Se o provedor também espera usar o alocador de memória OLE, ele deve chamar o método **IUnknown::AddRef** do objeto alocador apontado pelo parâmetro _lpMalloc._ 
  
Para obter mais informações sobre como **escrever XPProviderInit**, consulte [Inicializando o provedor de transporte](initializing-the-transport-provider.md). Para obter mais informações sobre funções de ponto de entrada, consulte [Implementando uma função de](implementing-a-service-provider-entry-point-function.md)ponto de entrada do provedor de serviços. 
  
## <a name="see-also"></a>Confira também



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

