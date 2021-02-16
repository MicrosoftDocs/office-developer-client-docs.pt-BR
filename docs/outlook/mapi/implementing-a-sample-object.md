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
# <a name="implementing-a-sample-object"></a><span data-ttu-id="883aa-103">Implementar um objeto de exemplo</span><span class="sxs-lookup"><span data-stu-id="883aa-103">Implementing a sample object</span></span>

<span data-ttu-id="883aa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="883aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="883aa-105">Aconselhe objetos sink — objetos que suportam a interface [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) — são objetos MAPI que os aplicativos cliente implementam para processar notificações.</span><span class="sxs-lookup"><span data-stu-id="883aa-105">Advise sink objects — objects that support the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface — are MAPI objects that client applications implement for processing notifications.</span></span> <span data-ttu-id="883aa-106">**IMAPIAdviseSink** herda diretamente de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) e contém apenas um método, **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="883aa-106">**IMAPIAdviseSink** inherits directly from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) and contains only one method, **OnNotify**.</span></span> <span data-ttu-id="883aa-107">Portanto, para implementar um objeto sink de aconselhe, um cliente cria código para os três métodos **em IUnknown** e [para OnNotify](imapiadvisesink-onnotify.md).</span><span class="sxs-lookup"><span data-stu-id="883aa-107">Therefore, to implement an advise sink object, a client creates code for the three methods in **IUnknown** and for [OnNotify](imapiadvisesink-onnotify.md).</span></span>
  
<span data-ttu-id="883aa-108">O arquivo de header Mapidefs.h define uma implementação de interface **IMAPIAdviseSink** usando DECLARE_MAPI_INTERFACE **,** da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="883aa-108">The Mapidefs.h header file defines an **IMAPIAdviseSink** interface implementation by using **DECLARE_MAPI_INTERFACE**, as follows:</span></span>
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

<span data-ttu-id="883aa-109">Os clientes que implementam objetos sink de alerta podem definir suas interfaces em seus objetos manualmente ou com as macros **MAPI_IUNKNOWN_METHODS** e **MAPI_IMAPIADVISESINK_METHODS** cliente.</span><span class="sxs-lookup"><span data-stu-id="883aa-109">Clients that implement advise sink objects can define their interfaces in their objects manually or with the **MAPI_IUNKNOWN_METHODS** and **MAPI_IMAPIADVISESINK_METHODS** macros.</span></span> <span data-ttu-id="883aa-110">Implementadores de objeto devem usar as macros de interface sempre que possível para garantir a consistência entre objetos e para economizar tempo e esforço.</span><span class="sxs-lookup"><span data-stu-id="883aa-110">Object implementers should use the interface macros whenever possible to ensure consistency across objects and to save time and effort.</span></span> 
  
<span data-ttu-id="883aa-111">Implementar os métodos [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) e [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) é relativamente simples porque normalmente são necessárias apenas algumas linhas de código.</span><span class="sxs-lookup"><span data-stu-id="883aa-111">Implementing the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods is relatively simple because typically only a few lines of code are needed.</span></span> <span data-ttu-id="883aa-112">Portanto, os clientes e provedores de serviços que implementam objetos podem fazer suas implementações **addRef** e **Release** em linha.</span><span class="sxs-lookup"><span data-stu-id="883aa-112">Therefore, clients and service providers that implement objects can make their **AddRef** and **Release** implementations inline.</span></span> <span data-ttu-id="883aa-113">O código a seguir mostra como definir um objeto sink de consultoria C++ com implementações em linha de **AddRef** e **Release**.</span><span class="sxs-lookup"><span data-stu-id="883aa-113">The following code shows how to define a C++ advise sink object with inline implementations of **AddRef** and **Release**.</span></span>
  
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

<span data-ttu-id="883aa-114">Em C, o objeto sink advise é composto pelos seguintes elementos:</span><span class="sxs-lookup"><span data-stu-id="883aa-114">In C, the advise sink object is composed of the following elements:</span></span>
  
- <span data-ttu-id="883aa-115">Um ponteiro para uma vtable que contém ponteiros para implementações de cada um dos métodos **em IUnknown** e **IMAPIAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="883aa-115">A pointer to a vtable that contains pointers to implementations of each of the methods in **IUnknown** and **IMAPIAdviseSink**.</span></span>
    
- <span data-ttu-id="883aa-116">Membros de dados.</span><span class="sxs-lookup"><span data-stu-id="883aa-116">Data members.</span></span>
    
<span data-ttu-id="883aa-117">O exemplo de código a seguir mostra como definir um objeto sink advise em C e construir sua vtable.</span><span class="sxs-lookup"><span data-stu-id="883aa-117">The following code example shows how to define an advise sink object in C and construct its vtable.</span></span> 
  
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

<span data-ttu-id="883aa-118">Depois de declarar um objeto em C, você deve inicializá-lo definindo o ponteiro vtable para o endereço da vtable construída, conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="883aa-118">After you declare an object in C, you must initialize it by setting the vtable pointer to the address of the constructed vtable, as shown in the following code:</span></span>
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a><span data-ttu-id="883aa-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="883aa-119">See also</span></span>

- [<span data-ttu-id="883aa-120">Visão geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="883aa-120">MAPI Property Overview</span></span>](mapi-property-overview.md)
- [<span data-ttu-id="883aa-121">Implementando objetos MAPI</span><span class="sxs-lookup"><span data-stu-id="883aa-121">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

