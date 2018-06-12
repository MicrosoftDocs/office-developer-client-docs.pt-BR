---
title: Implementação de um objeto de amostra
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 85de8dd7211fa19b7cdbda9f5ced1f00a736ca9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767405"
---
# <a name="implementing-a-sample-object"></a>Implementação de um objeto de amostra

**Aplica-se a**: Outlook 
  
Objetos de coletor de eventos de aviso — objetos que suportam o [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) interface — são objetos de MAPI que aplicativos cliente implementam para processamento de notificações. **IMAPIAdviseSink** herda diretamente da [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) e contém apenas um método, **OnNotify**. Portanto, para implementar um objeto de coletor de eventos advise, um cliente cria código para os três métodos **IUnknown** e [OnNotify](imapiadvisesink-onnotify.md).
  
O arquivo de cabeçalho Mapidefs.h define uma implementação de interface **IMAPIAdviseSink** usando **DECLARE_MAPI_INTERFACE**, da seguinte maneira:
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

Clientes que implementam aconselhe os objetos de coletor de eventos podem definir suas interfaces nos seus objetos manualmente ou com as macros **MAPI_IUNKNOWN_METHODS** e **MAPI_IMAPIADVISESINK_METHODS** . Implementadores do objeto devem usar as macros de interface sempre que possível para garantir a consistência entre objetos e para economizar tempo e esforço. 
  
Implementar os métodos [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) e [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) é relativamente simple, porque geralmente apenas algumas linhas de código são necessárias. Portanto, clientes e provedores de serviços que implementam objetos podem fazer sua embutida de implementações **AddRef** e **Release** . O código a seguir mostra como definir um C++ avise o objeto coletor de eventos com embutida implementações de **AddRef** e **Release**.
  
```cpp
class  CMAPIAdviseSink : public IMAPIAdviseSink
{
public:
    STDMETHODIMP QueryInterface
                    (REFIID                     riid,
                     LPVOID *                   ppvObj);
    inline STDMETHODIMP_(ULONG) AddRef
                    () { InterlockedIncrement(m_cRef);
                         ++m_cRef;
                         InterlockedDecrement(m_cRef);
                         return m_cRef; };
    inline STDMETHODIMP_(ULONG) Release
                    () { InterlockedIncrement(m_cRef);
                         ULONG ulCount = --m_cRef;
                         InterlockedDecrement(m_cRef);
                         if (!ulCount)  delete this;
                         return ulCount;};
    MAPI_IMAPIADVISESINK_METHODS(IMPL);
    BOOL WINAPI AddConnection (LPMDB pMDBObj, ULONG ulConnection);
    void WINAPI RemoveAllLinks (LPMDB pMDBObj);
// Constructors and destructors.
public :
    inline CMAPIAdviseSink  (CStoreClient * pStore)
                            { m_cRef = 1;
                              m_ulConnection = 0;
                              m_pStore = pStore;
                              AddRef;};
    ~CMAPIAdviseSink () {Release};
private :
    ULONG               m_cRef;
    CStoreClient *      m_pStore;
    ULONG               m_ulConnection;
};
 
```

C, o objeto coletor de eventos advise consiste nos seguintes elementos:
  
- Um ponteiro para uma vtable que contém ponteiros para implementações de cada um dos métodos na **IUnknown** e **IMAPIAdviseSink**.
    
- Membros de dados.
    
O exemplo de código a seguir mostra como definir um objeto de coletor de eventos advise em C e construir sua vtable. 
  
```cpp
// Object definition.
typedef struct _ADVISESINK
{
    const ADVISE_Vtbl FAR *    lpVtbl;
    ULONG             cRef;
    STORECLIENT      *pStore;
    ULONG             ulConnection;
} ADVISESINK, *LPADVISESINK;
// vtable definition.
static const ADVISE_Vtbl vtblADVISE =
{
    ADVISE_QueryInterface,
    ADVISE_AddRef,
    ADVISE_Release,
    ADVISE_OnNotify
};
 
```

Depois que você declarar um objeto em C, inicializá-lo, definindo o ponteiro vtable como o endereço do vtable construído, conforme mostrado no seguinte código:
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a>Confira também

- [Vis�o geral da propriedade MAPI](mapi-property-overview.md)
- [Implementar objetos de MAPI](implementing-mapi-objects.md)

