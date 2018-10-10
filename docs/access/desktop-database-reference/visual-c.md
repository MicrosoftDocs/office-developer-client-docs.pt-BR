---
title: Visual C++ (referência de banco de dados da área de trabalho do Access)
TOCTitle: Visual C++
ms:assetid: 31d27968-e7bd-02fa-efad-26039bea30b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249091(v=office.15)
ms:contentKeyID: 48544062
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1a12304cc30e9e653f1cb10343cac390395961fa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462885"
---
# <a name="visual-c"></a><span data-ttu-id="87e5b-102">Visual C++</span><span class="sxs-lookup"><span data-stu-id="87e5b-102">Visual C++</span></span>


<span data-ttu-id="87e5b-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="87e5b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="87e5b-p101">Esta é uma descrição esquemática de como instanciar eventos do ADO no Microsoft Visual C++. Consulte o [Exemplo do modelo de eventos do ADO (VC++)](ado-events-model-example-vc.md) para obter uma descrição completa.</span><span class="sxs-lookup"><span data-stu-id="87e5b-p101">This is a schematic description of how to instantiate ADO events in Microsoft Visual C++. See [ADO Events Model Example (VC++)](ado-events-model-example-vc.md) for a complete description.</span></span>

<span data-ttu-id="87e5b-106">Crie classes derivadas das interfaces **ConnectionEventsVt** e **RecordsetEventsVt** encontradas no arquivo adoint.h.</span><span class="sxs-lookup"><span data-stu-id="87e5b-106">Create classes derived from the **ConnectionEventsVt** and **RecordsetEventsVt** interfaces found in the file adoint.h.</span></span>

```cpp 
 
// BeginEventExampleVC01 
class CConnEvent : public ConnectionEventsVt 
{ 
 public: 
 STDMETHODIMP InfoMessage( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection); 
... 
} 
 
class CRstEvent : public RecordsetEventsVt 
{ 
 public: 
 STDMETHODIMP WillChangeField( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset); 
... 
} 
// EndEventExampleVC01 
```

<span data-ttu-id="87e5b-107">Implemente cada um dos métodos do manipulador de eventos nas duas classes.</span><span class="sxs-lookup"><span data-stu-id="87e5b-107">Implement each of the event-handler methods in both classes.</span></span> <span data-ttu-id="87e5b-108">É suficiente que cada método meramente retorna um HRESULT de S\_Okey.</span><span class="sxs-lookup"><span data-stu-id="87e5b-108">It is sufficient that each method merely return an HRESULT of S\_OK.</span></span> <span data-ttu-id="87e5b-109">No entanto, quando você informar que os manipuladores de eventos estão disponíveis, eles serão chamados continuamente por padrão.</span><span class="sxs-lookup"><span data-stu-id="87e5b-109">However, when you make it known that your event handlers are available, they will be called continuously by default.</span></span> <span data-ttu-id="87e5b-110">Em vez disso, convém não solicitar mais notificações após a primeira vez definindo **adStatus** como **adStatusUnwantedEvent**.</span><span class="sxs-lookup"><span data-stu-id="87e5b-110">Instead, you might want to request no further notification after the first time by setting **adStatus** to **adStatusUnwantedEvent**.</span></span>

```cpp 
 
// BeginEventExampleVC02 
STDMETHODIMP CConnEvent::ConnectComplete( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADOConnection *pConnection) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
// EndEventExampleVC02 
```

<span data-ttu-id="87e5b-p103">As classes de evento são herdadas de **IUnknown**; portanto, você também deve implementar os métodos **QueryInterface**, **AddRef** e **Release**. Além disso, implemente construtores e destrutores de classes. Escolha as ferramentas do Visual C++ com as quais você esteja mais familiarizado, a fim de simplificar essa parte da tarefa.</span><span class="sxs-lookup"><span data-stu-id="87e5b-p103">The event classes inherit from **IUnknown**, so you must also implement the **QueryInterface**, **AddRef**, and **Release** methods. Also implement class constructors and destructors. Choose the Visual C++ tools with which you are most comfortable to simplify this part of the task.</span></span>

<span data-ttu-id="87e5b-p104">Informe que os manipuladores de eventos estão disponíveis, executando **QueryInterface** nos objetos [Recordset](recordset-object-ado.md) e [Connection](connection-object-ado.md) das interfaces **IConnectionPointContainer** e **IConnectionPoint**. Em seguida, execute **IConnectionPoint::Advise** para cada classe.</span><span class="sxs-lookup"><span data-stu-id="87e5b-p104">Make it known that your event handlers are available by issuing **QueryInterface** on the [Recordset](recordset-object-ado.md) and [Connection](connection-object-ado.md) objects for the **IConnectionPointContainer** and **IConnectionPoint** interfaces. Then issue **IConnectionPoint::Advise** for each class.</span></span>

<span data-ttu-id="87e5b-116">Por exemplo, suponha que você esteja usando uma função booleana que retorne **True** se ela informar um objeto **Recordset** de que você tem manipuladores de eventos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="87e5b-116">For example, assume you are using a Boolean function that returns **True** if it successfully informs a **Recordset** object that you have event handlers available.</span></span>

```cpp 
 
// BeginEventExampleVC03 
HRESULT hr; 
DWORD dwEvtClass; 
IConnectionPointContainer *pCPC = NULL; 
IConnectionPoint *pCP = NULL; 
CRstEvent *pRStEvent = NULL; 
... 
_RecordsetPtr pRs; 
pRs.CreateInstance(__uuidof(Recordset)); 
pRStEvent = new CRstEvent; 
if (pRStEvent == NULL) return FALSE; 
... 
hr = pRs->QueryInterface(IID_IConnectionPointContainer, (LPVOID *)&pCPC); 
if (FAILED(hr)) return FALSE; 
hr = pCPC->FindConnectionPoint(RecordsetEvents, &pCP); 
pCPC->Release(); // Always Release now, even before checking. 
if (FAILED(hr)) return FALSE; 
hr = pCP->Advise(pRstEvent, &dwEvtClass); //Turn on event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
return TRUE; 
... 
// EndEventExampleVC03 
```

<span data-ttu-id="87e5b-117">Nesse ponto, os eventos da família **RecordsetEvent** são ativados e seus métodos serão chamados quando ocorrerem eventos de **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="87e5b-117">At this point, events for the **RecordsetEvent** family are enabled and your methods will be called as **Recordset** events occur.</span></span>

<span data-ttu-id="87e5b-118">Posteriormente, quando você quiser tornar os manipuladores de eventos indisponíveis, obtenha o ponto de conexão novamente e execute o método **IConnectionPoint::Unadvise**.</span><span class="sxs-lookup"><span data-stu-id="87e5b-118">Later, when you want to make your event handlers unavailable, get the connection point again and issue the **IConnectionPoint::Unadvise** method.</span></span>

```cpp 
 
// BeginEventExampleVC04 
... 
hr = pCP->Unadvise(dwEvtClass); //Turn off event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
// EndEventExampleVC04 
```

<span data-ttu-id="87e5b-119">Você deve liberar interfaces e destruir objetos de classe conforme o necessário.</span><span class="sxs-lookup"><span data-stu-id="87e5b-119">You must release interfaces and destroy class objects as appropriate.</span></span>

<span data-ttu-id="87e5b-120">O código a seguir mostra um exemplo completo de uma classe de coletor de eventos **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="87e5b-120">The following code shows a complete example of a **Recordset** Event sink class.</span></span>

```vb 
 
// BeginEventExampleVC05 
#include <adoint.h> 
 
class CADORecordsetEvents : public RecordsetEventsVt 
{ 
public : 
 
 ULONG m_ulRefCount; 
 CADORecordsetEvents():m_ulRefCount(1){} 
 
 STDMETHOD(QueryInterface)(REFIID iid, LPVOID * ppvObject) 
 { 
 if (IsEqualIID(__uuidof(IUnknown), iid) || 
 IsEqualIID(__uuidof(RecordsetEventsVt), iid)) 
 { 
 *ppvObject = this; 
 return S_OK; 
 } 
 else 
 return E_NOINTERFACE; 
 } 
 
 STDMETHOD_(ULONG, AddRef)() 
 { 
 return m_ulRefCount++; 
 } 
 
 STDMETHOD_(ULONG, Release)() 
 { 
 if (--m_ulRefCount == 0) 
 { 
 delete this; 
 return 0; 
 } 
 else 
 return m_ulRefCount; 
 } 
 
 
 STDMETHOD(WillChangeField)( 
 LONG cFields, 
 VARIANT Fields, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FieldChangeComplete)( 
 LONG cFields, 
 VARIANT Fields, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(WillChangeRecord)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(RecordChangeComplete)( 
 EventReasonEnum adReason, 
 LONG cRecords, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillChangeRecordset)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(RecordsetChangeComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(WillMove)( 
 EventReasonEnum adReason, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(MoveComplete)( 
 EventReasonEnum adReason, 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(EndOfRecordset)( 
 VARIANT_BOOL *fMoreData, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 STDMETHOD(FetchProgress)( 
 long Progress, 
 long MaxProgress, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
 
 STDMETHOD(FetchComplete)( 
 ADOError *pError, 
 EventStatusEnum *adStatus, 
 _ADORecordset *pRecordset) 
 { 
 *adStatus = adStatusUnwantedEvent; 
 return S_OK; 
 } 
 
}; 
// EndEventExampleVC05 
```

