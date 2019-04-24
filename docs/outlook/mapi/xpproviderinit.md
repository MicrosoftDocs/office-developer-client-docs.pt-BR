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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325652"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicializa um provedor de transporte para operação.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi. h  <br/> |
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
  
> no A instância da biblioteca de vínculo dinâmico (DLL) do provedor de transporte que o MAPI usou quando carregou a DLL.
    
 _lpMalloc_
  
> no Ponteiro para um objeto de alocador de memória expondo a interface **IMalloc** do OLE. O provedor de transporte pode precisar usar esse método de alocação quando estiver trabalhando com determinadas interfaces, como **IStream**. 
    
 _lpAllocateBuffer_
  
> no Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , a ser usado para alocar memória. 
    
 _lpAllocateMore_
  
> no Ponteiro para a função [MAPIAllocateMore](mapiallocatemore.md) , a ser usado para alocar memória adicional. 
    
 _lpFreeBuffer_
  
> no Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , a ser usado para liberar memória. 
    
 _ulFlags_
  
> no Bitmask de sinalizadores. O seguinte sinalizador pode ser definido:
    
MAPI_NT_SERVICE 
  
> O provedor está sendo carregado no contexto de um serviço do Windows, um tipo especial de processo sem acesso a qualquer interface do usuário. 
    
 _ulMAPIVer_
  
> no Número da versão da interface do provedor de serviços (SPI) que MAPI. dll usa. Para o número da versão atual, confira o arquivo de cabeçalho Mapispi. h. 
    
 _lpulProviderVer_
  
> bota Ponteiro para o número da versão do SPI que este provedor de transporte usa. 
    
 _lppXPProvider_
  
> bota Ponteiro para um ponteiro para o objeto do provedor de transporte inicializado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados. 
    
MAPI_E_VERSION 
  
> A versão SPI que está sendo usada pelo MAPI não é compatível com o SPI que está sendo usado por este provedor.
    
## <a name="remarks"></a>Comentários

MAPI chama a função de ponto de entrada **XPProviderInit** para inicializar um provedor de transporte após um logon de cliente. **XPProviderInit** é chamado uma vez para cada provedor de transporte especificado no perfil do cliente. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Um provedor de transporte deve implementar **XPProviderInit** como uma função de ponto de entrada na DLL do provedor. A implementação deve ser baseada no protótipo de função **XPPROVIDERINIT** , também especificado em Mapispi. h. MAPI define **XPPROVIDERINIT** para usar o tipo de chamada de inicialização MAPI padrão, STDMAPIINITCALLTYPE, que faz com que o **XPPROVIDERINIT** siga a Convenção de chamada do cdecl. Uma vantagem do CDECL é que as chamadas podem ser tentadas mesmo se o número de parâmetros de chamada não corresponder ao número de parâmetros definidos. 
  
Um provedor pode ser inicializado várias vezes como resultado de aparecer em vários perfis em uso simultâneo ou de ser exibido mais de uma vez no mesmo perfil. Como o objeto Provider contém contexto, **XPProviderInit** deve retornar um objeto Provider diferente no _lppXPProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo. 
  
O provedor de transporte deve usar as funções apontadas por _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria da alocação de memória e desalocação. Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos cliente ao chamar interfaces de objeto, como [IMAPIProp::](imapiprop-getprops.md) GetProps e IMAPITable [:: QueryRows](imapitable-queryrows.md). Se o provedor também espera usar o alocador de memória OLE, ele deve chamar o método **IUnknown:: AddRef** do objeto de alocador apontado pelo parâmetro _lpMalloc_ . 
  
Para obter mais informações sobre a gravação de **XPProviderInit**, consulte [inicializando o provedor de transporte](initializing-the-transport-provider.md). Para obter mais informações sobre funções de ponto de entrada, consulte [implementando uma função de ponto de entrada do provedor de serviços](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Confira também



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

