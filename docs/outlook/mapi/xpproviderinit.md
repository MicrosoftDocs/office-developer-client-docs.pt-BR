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
ms.openlocfilehash: 38b60180ae7c417bf34998e72f96b353ace02859
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592532"
---
# <a name="xpproviderinit"></a>XPProviderInit

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicializa a um provedor de transporte para a operação.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Implementada por:  <br/> |Provedores de transporte  <br/> |
|Chamado pelo:  <br/> |MAPI  <br/> |
   
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
  
> [in] A instância de biblioteca de vínculo dinâmico do provedor de transporte (DLL) que MAPI usada quando ele carregado a DLL.
    
 _lpMalloc_
  
> [in] Ponteiro para um objeto de alocador de memória expondo a interface OLE **IMalloc** . Talvez seja necessário usar esse método de alocação ao trabalhar com certas interfaces como **IStream**o provedor de transporte. 
    
 _lpAllocateBuffer_
  
> [in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória. 
    
 _lpAllocateMore_
  
> [in] Ponteiro para a função de [MAPIAllocateMore](mapiallocatemore.md) , para ser usado para alocar memória adicional. 
    
 _lpFreeBuffer_
  
> [in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória. 
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores. O seguinte sinalizador pode ser definido:
    
MAPI_NT_SERVICE 
  
> O provedor está sendo carregado no contexto de um serviço do Windows, um tipo especial de processo sem acesso a qualquer interface do usuário. 
    
 _ulMAPIVer_
  
> [in] Número de versão da interface de provedor do serviço (SPI) que usa MAPI. dll. Para o número da versão atual, consulte o arquivo de cabeçalho Mapispi.h. 
    
 _lpulProviderVer_
  
> [out] Ponteiro para o número de versão da SPI que usa esse provedor de transporte. 
    
 _lppXPProvider_
  
> [out] Ponteiro para um ponteiro para o objeto de provedor de transporte inicializada.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores. 
    
MAPI_E_VERSION 
  
> A versão EDA sendo usada pelo MAPI não é compatível com o SPI sendo usado por este provedor.
    
## <a name="remarks"></a>Comentários

MAPI chama a função do ponto de entrada **XPProviderInit** ao inicializar um provedor de transporte seguindo um logon do cliente. **XPProviderInit** é chamado uma vez para cada provedor de transporte especificado no perfil do cliente. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Um provedor de transporte deve implementar **XPProviderInit** como uma função de ponto de entrada na DLL do provedor. A implementação deve se basear no protótipo de função **XPPROVIDERINIT** , também especificado em Mapispi.h. MAPI define **XPPROVIDERINIT** para usar o MAPI inicialização chamada tipo padrão, STDMAPIINITCALLTYPE, que faz com que o **XPProviderInit** a seguir a convenção de chamada CDECL. Uma vantagem da convenção CDECL é que chamadas podem ser tentadas, mesmo se o número de chamada de parâmetros não coincide com o número de parâmetros definidos. 
  
Um provedor pode ser inicializado várias vezes como resultado que aparecem em vários perfis em uso simultâneo ou do que aparecem mais de uma vez no mesmo perfil. Porque o objeto de provedor contém contexto, **XPProviderInit** deve retornar um objeto de provedor diferente em _lppXPProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo. 
  
O provedor de transporte deve usar as funções apontadas pela _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria dos alocação de memória e desalocação. Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos do cliente, ao chamar interfaces de objeto, como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md). Se o provedor de espera-se também usar o alocador de memória OLE, ele deve chamar o método **AddRef** do objeto alocador apontado pelo parâmetro _lpMalloc_ . 
  
Para obter mais informações sobre como escrever **XPProviderInit**, consulte [inicializar o provedor de transporte](initializing-the-transport-provider.md). Para obter mais informações sobre funções de ponto de entrada, consulte [Implementando uma função de ponto de entrada do serviço provedor](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Confira também



[ABProviderInit](abproviderinit.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[MSProviderInit](msproviderinit.md)

