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
ms.openlocfilehash: 9a5f8b44f9d795282ccfd61fd32a306c5478ed21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416234"
---
# <a name="msproviderinit"></a>MSProviderInit

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicializa um provedor de armazenamento de mensagens para operação.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Implementado por:  <br/> |Provedores de armazenamento de mensagens  <br/> |
|Chamado por:  <br/> |MAPI  <br/> |
   
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
  
> [in] A instância da biblioteca de vínculo dinâmico (DLL) do provedor de armazenamento de mensagens que o MAPI usou ao vincular. 
    
 _lpMalloc_
  
> [in] Ponteiro para um objeto alocador de memória expondo a interface **IMalloc OLE.** O provedor de armazenamento de mensagens pode precisar usar esse método de alocação ao trabalhar com determinadas interfaces, como **IStream**. 
    
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
  
> [in] Número da versão da interface do provedor de serviços (SPI) que o MAPI usa. Para o número da versão atual, consulte o arquivo de header Mapispi.h. 
    
 _lpulProviderVer_
  
> [out] Ponteiro para o número de versão do SPI que esse provedor de armazenamento de mensagens usa. 
    
 _lppMSProvider_
  
> [out] Ponteiro para um ponteiro para o objeto de provedor de armazenamento de mensagens inicializado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados. 
    
MAPI_E_VERSION 
  
> A versão SPI usada por MAPI não é compatível com o SPI usado por esse provedor.
    
## <a name="remarks"></a>Comentários

MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Um provedor de armazenamento de mensagens deve implementar **MSProviderInit** como uma função de ponto de entrada na DLL do provedor. A implementação deve ser baseada no protótipo **de função MSPROVIDERINIT,** também especificado em MAPISPI.H. MAPI define **MSPROVIDERINIT** para usar o tipo de chamada de inicialização mapi padrão, STDMAPIINITCALLTYPE, que faz com que **MSProviderInit** siga a convenção de chamada CDECL. Uma vantagem do CDECL é que as chamadas podem ser tentadas mesmo se o número de parâmetros de chamada não corresponder ao número de parâmetros definidos. 
  
Um provedor pode ser inicializado várias vezes, como resultado de aparecer em vários perfis em uso simultâneo ou de aparecer mais de uma vez no mesmo perfil. Como o objeto do provedor contém contexto, **MSProviderInit** deve retornar um objeto de provedor diferente em  _lppMSProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo. 
  
A DLL do provedor não deve ser vinculada a Mapix.dll. Em vez disso, ele deve usar esses ponteiros para alocação de memória ou desalocação. 
  
O provedor de armazenamento de mensagens deve usar as funções apontadas por  _lpAllocateBuffer_,  _lpAllocateMore_ e  _lpFreeBuffer_ para a maioria da alocação e alocação de memória. Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos cliente ao chamar interfaces de objeto, como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md). Se o provedor também espera usar o alocador de memória OLE, ele deve chamar o método **IUnknown::AddRef** do objeto alocador apontado pelo parâmetro _lpMalloc._ 
  
Para obter mais informações sobre como **escrever MSProviderInit**, consulte [Carregando provedores de armazenamento de mensagens.](loading-message-store-providers.md) Para obter mais informações sobre funções de ponto de entrada, consulte [Implementando uma função de](implementing-a-service-provider-entry-point-function.md)ponto de entrada do provedor de serviços. 
  
## <a name="see-also"></a>Confira também



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

