---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cf1febe89c49b29cdfaf8d27760c4fb27b4c4990
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768147"
---
# <a name="msproviderinit"></a>MSProviderInit

  
  
**Aplica-se a**: Outlook 
  
Inicializa a um provedor de armazenamento de mensagem para a operação.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Implementada por:  <br/> |Provedores de armazenamento de mensagem  <br/> |
|Chamado pelo:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT MSProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPMSPROVIDER FAR * lppMSProvider
);
```

## <a name="parameters"></a>Parâmetros

 _hInstance_
  
> [in] A instância da mensagem armazenar biblioteca de vínculo dinâmico do provedor (DLL) que MAPI usado quando vinculado. 
    
 _lpMalloc_
  
> [in] Ponteiro para um objeto de alocador de memória expondo a interface OLE **IMalloc** . Talvez seja necessário usar esse método de alocação ao trabalhar com certas interfaces como **IStream**o provedor de armazenamento de mensagem. 
    
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
  
> [in] Número de versão da interface de provedor do serviço (SPI) que usa MAPI. Para o número da versão atual, consulte o arquivo de cabeçalho Mapispi.h. 
    
 _lpulProviderVer_
  
> [out] Ponteiro para o número de versão da SPI que usa esse provedor de repositório de mensagem. 
    
 _lppMSProvider_
  
> [out] Ponteiro para um ponteiro para o objeto de provedor de armazenamento de mensagem inicializada.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores. 
    
MAPI_E_VERSION 
  
> A versão EDA sendo usada pelo MAPI não é compatível com o SPI sendo usado por este provedor.
    
## <a name="remarks"></a>Comentários

MAPI chama a função do ponto de entrada **MSProviderInit** ao inicializar um provedor de armazenamento de mensagem seguindo um logon do cliente. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Um provedor de armazenamento de mensagem deve implementar **MSProviderInit** como uma função de ponto de entrada na DLL do provedor. A implementação deve se basear no protótipo de função **MSPROVIDERINIT** , também especificado em MAPISPI. H. MAPI define **MSPROVIDERINIT** para usar o MAPI inicialização chamada tipo padrão, STDMAPIINITCALLTYPE, que faz com que o **MSProviderInit** a seguir a convenção de chamada CDECL. Uma vantagem da convenção CDECL é que chamadas podem ser tentadas, mesmo se o número de chamada de parâmetros não coincide com o número de parâmetros definidos. 
  
Um provedor pode ser inicializado várias vezes, como resultado que aparecem em vários perfis em uso simultâneo ou do que aparecem mais de uma vez no mesmo perfil. Porque o objeto de provedor contém contexto, **MSProviderInit** deve retornar um objeto de provedor diferente em _lppMSProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo. 
  
Não deve ser vinculado a DLL do provedor com Mapix.dll. Em vez disso, ele deve usar esses ponteiros de alocação de memória ou desalocação. 
  
O provedor de armazenamento de mensagem deve usar as funções apontadas pela _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria dos alocação de memória e desalocação. Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos do cliente, ao chamar interfaces de objeto, como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md). Se o provedor de espera-se também usar o alocador de memória OLE, ele deve chamar o método **AddRef** do objeto alocador apontado pelo parâmetro _lpMalloc_ . 
  
Para obter mais informações sobre como escrever **MSProviderInit**, consulte [Carregando provedores de armazenamento de mensagem](loading-message-store-providers.md). Para obter mais informações sobre funções de ponto de entrada, consulte [Implementando uma função de ponto de entrada do serviço provedor](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Confira também



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

