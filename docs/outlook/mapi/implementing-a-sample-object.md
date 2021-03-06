---
title: Implementar um objeto de exemplo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a681e68c0718e49da331946d75ecb7b4fab7afe2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332827"
---
# <a name="implementing-a-sample-object"></a>Implementar um objeto de exemplo

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aconselhe objetos sink — objetos que suportam a interface [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) — são objetos MAPI que os aplicativos cliente implementam para processar notificações. **IMAPIAdviseSink** herda diretamente de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) e contém apenas um método, **OnNotify**. Portanto, para implementar um objeto sink de aconselhe, um cliente cria código para os três métodos **em IUnknown** e [para OnNotify](imapiadvisesink-onnotify.md).
  
O arquivo de header Mapidefs.h define uma implementação de interface **IMAPIAdviseSink** usando DECLARE_MAPI_INTERFACE **,** da seguinte forma:
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

Os clientes que implementam objetos sink de alerta podem definir suas interfaces em seus objetos manualmente ou com as macros **MAPI_IUNKNOWN_METHODS** e **MAPI_IMAPIADVISESINK_METHODS** cliente. Implementadores de objeto devem usar as macros de interface sempre que possível para garantir a consistência entre objetos e para economizar tempo e esforço. 
  
Implementar os métodos [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) e [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) é relativamente simples porque normalmente são necessárias apenas algumas linhas de código. Portanto, os clientes e provedores de serviços que implementam objetos podem fazer suas implementações **addRef** e **Release** em linha. O código a seguir mostra como definir um objeto sink de consultoria C++ com implementações em linha de **AddRef** e **Release**.
  
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

Em C, o objeto sink advise é composto pelos seguintes elementos:
  
- Um ponteiro para uma vtable que contém ponteiros para implementações de cada um dos métodos **em IUnknown** e **IMAPIAdviseSink**.
    
- Membros de dados.
    
O exemplo de código a seguir mostra como definir um objeto sink advise em C e construir sua vtable. 
  
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

Depois de declarar um objeto em C, você deve inicializá-lo definindo o ponteiro vtable para o endereço da vtable construída, conforme mostrado no código a seguir:
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a>Confira também

- [Visão geral da propriedade MAPI](mapi-property-overview.md)
- [Implementando objetos MAPI](implementing-mapi-objects.md)

