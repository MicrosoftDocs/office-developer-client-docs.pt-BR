---
title: Visual C++ (referência de banco de dados da área de trabalho do Access)
TOCTitle: Visual C++
ms:assetid: 31d27968-e7bd-02fa-efad-26039bea30b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249091(v=office.15)
ms:contentKeyID: 48544062
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e0285fd190ade398d4e5c834296313edf9ef7b3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870937"
---
# <a name="visual-c"></a>Visual C++


**Aplica-se a**: Access 2013, o Office 2013

Esta é uma descrição esquemática de como instanciar eventos do ADO no Microsoft Visual C++. Consulte o [exemplo de modelo de eventos do ADO (VC + +)](ado-events-model-example-vc.md) para obter uma descrição completa.

Crie classes derivadas das interfaces **ConnectionEventsVt** e **RecordsetEventsVt** encontradas no arquivo adoint.h.

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

Implemente cada um dos métodos do manipulador de eventos nas duas classes. É suficiente que cada método meramente retorna um HRESULT de S\_Okey. No entanto, quando você informar que os manipuladores de eventos estão disponíveis, eles serão chamados continuamente por padrão. Em vez disso, convém não solicitar mais notificações após a primeira vez definindo **adStatus** como **adStatusUnwantedEvent**.

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

As classes de evento são herdadas de **IUnknown**; portanto, você também deve implementar os métodos **QueryInterface**, **AddRef** e **Release**. Além disso, implemente construtores e destrutores de classes. Escolha as ferramentas do Visual C++ com as quais você esteja mais familiarizado, a fim de simplificar essa parte da tarefa.

Informe que os manipuladores de eventos estão disponíveis, executando **QueryInterface** nos objetos [Recordset](recordset-object-ado.md) e [Connection](connection-object-ado.md) das interfaces **IConnectionPointContainer** e **IConnectionPoint**. Em seguida, execute **IConnectionPoint::Advise** para cada classe.

Por exemplo, suponha que você esteja usando uma função booleana que retorne **True** se ela informar um objeto **Recordset** de que você tem manipuladores de eventos disponíveis.

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

Nesse ponto, os eventos da família **RecordsetEvent** são ativados e seus métodos serão chamados quando ocorrerem eventos de **Recordset**.

Posteriormente, quando você quiser tornar os manipuladores de eventos indisponíveis, obtenha o ponto de conexão novamente e execute o método **IConnectionPoint::Unadvise**.

```cpp 
 
// BeginEventExampleVC04 
... 
hr = pCP->Unadvise(dwEvtClass); //Turn off event support. 
pCP->Release(); 
if (FAILED(hr)) return FALSE; 
... 
// EndEventExampleVC04 
```

Você deve liberar interfaces e destruir objetos de classe conforme o necessário.

O código a seguir mostra um exemplo completo de uma classe de coletor de eventos **Recordset**.

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

