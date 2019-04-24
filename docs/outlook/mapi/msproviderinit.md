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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342788"
---
# <a name="msproviderinit"></a>MSProviderInit

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicializa um provedor de armazenamento de mensagens para operação.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi. h  <br/> |
|Implementado por:  <br/> |Provedores de repositórios de mensagens  <br/> |
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
  
> no A instância da biblioteca de vínculo dinâmico (DLL) do provedor de repositório de mensagens usada ao ser vinculada. 
    
 _lpMalloc_
  
> no Ponteiro para um objeto de alocador de memória expondo a interface **IMalloc** do OLE. O provedor de repositório de mensagens pode precisar usar esse método de alocação quando estiver trabalhando com determinadas interfaces, como **IStream**. 
    
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
  
> no Número da versão da interface do provedor de serviços (SPI) que o MAPI usa. Para o número da versão atual, confira o arquivo de cabeçalho Mapispi. h. 
    
 _lpulProviderVer_
  
> bota Ponteiro para o número da versão do SPI que este provedor de armazenamento de mensagens usa. 
    
 _lppMSProvider_
  
> bota Ponteiro para um ponteiro para o objeto do provedor de armazenamento de mensagens inicializado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados. 
    
MAPI_E_VERSION 
  
> A versão SPI que está sendo usada pelo MAPI não é compatível com o SPI que está sendo usado por este provedor.
    
## <a name="remarks"></a>Comentários

MAPI chama a função de ponto de entrada **MSProviderInit** para inicializar um provedor de repositório de mensagens seguindo um logon de cliente. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Um provedor de repositório de mensagens deve implementar **MSProviderInit** como uma função de ponto de entrada na DLL do provedor. A implementação deve ser baseada no protótipo de função **MSPROVIDERINIT** , também especificado em MAPISPI. 0. MAPI define **MSPROVIDERINIT** para usar o tipo de chamada de inicialização MAPI padrão, STDMAPIINITCALLTYPE, que faz com que o **MSPROVIDERINIT** siga a Convenção de chamada do cdecl. Uma vantagem do CDECL é que as chamadas podem ser tentadas mesmo se o número de parâmetros de chamada não corresponder ao número de parâmetros definidos. 
  
Um provedor pode ser inicializado várias vezes, como resultado da apresentação de vários perfis em uso simultâneo ou de ser exibido mais de uma vez no mesmo perfil. Como o objeto Provider contém contexto, **MSProviderInit** deve retornar um objeto Provider diferente no _lppMSProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo. 
  
A DLL do provedor não deve ser vinculada a Mapix. dll. Em vez disso, ele deve usar esses ponteiros para alocação ou desalocação de memória. 
  
O provedor de repositório de mensagens deve usar as funções apontadas por _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria da alocação e desalocação de memória. Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos cliente ao chamar interfaces de objeto, como [IMAPIProp::](imapiprop-getprops.md) GetProps e IMAPITable [:: QueryRows](imapitable-queryrows.md). Se o provedor também espera usar o alocador de memória OLE, ele deve chamar o método **IUnknown:: AddRef** do objeto de alocador apontado pelo parâmetro _lpMalloc_ . 
  
Para obter mais informações sobre a gravação de **MSProviderInit**, consulte [carregando provedores de repositório de mensagens](loading-message-store-providers.md). Para obter mais informações sobre funções de ponto de entrada, consulte [implementando uma função de ponto de entrada do provedor de serviços](implementing-a-service-provider-entry-point-function.md). 
  
## <a name="see-also"></a>Confira também



[ABProviderInit](abproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[XPProviderInit](xpproviderinit.md)

