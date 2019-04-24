---
title: Eventos disponíveis e os dispids (Outlook exportados APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: Esta seção descreve os identificadores de expedição dos eventos que o Outlook disponibiliza.
ms.openlocfilehash: 31843a2eb8f91eabdc0dbf54a269270eb172baa7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316874"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Eventos disponíveis e os dispids (Outlook exportados APIs)

Esta seção descreve os identificadores de expedição dos eventos que o Outlook disponibiliza.
  
O Outlook expõe os seguintes identificadores de expedição (DispIds) para permitir que os suplementos do C++ escutem e manipulem os eventos correspondentes da função [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) . 
  
|**Constante**|**DISPID para evento**|**Descrição**|**Parâmetros**|**Comentários**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Usado para manipular o evento no nível do aplicativo da função **IDispatch:: Invoke** que é acionada antes de uma operação de impressão.  <br/> | Há dois parâmetros sem nome:  <br/>  O primeiro parâmetro é do tipo * * VT_BOOL|VT_BREF * *. Retornar **VARIANT_TRUE** neste parâmetro para cancelar o evento.  <br/>  O segundo parâmetro não é usado e deve ser ignorado.  <br/> |Este DISPID está disponível desde o Outlook 2010.  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Usado para lidar com o evento de nível de item a partir da função **IDispatch:: Invoke** que é acionada quando o Outlook conclui a leitura das propriedades do item.  <br/> |Há apenas um parâmetro _Cancel_ que é do tipo * * VT_BOOL|VT_BREF * *. Retornar **VARIANT_TRUE** neste parâmetro para cancelar a operação de leitura.  <br/> |Este DISPID está disponível desde o Outlook 2010.  <br/> Este evento corresponde ao evento Exchange Client Extensions (ECE) **IExchExtMessageEvents:: OnReadComplete**, e também ao evento **ReadComplete** que foi adicionado ao modelo de objeto desde o Outlook 2013.  <br/> |
   
Para obter um exemplo de como usar um DISPID para ouvir e lidar com um evento, consulte a `CAppEventListener::Invoke` função na solução do Outlook c++ descrita em [Implementing Outlook 2002/XP Event sinks in MFC C++ 2003 .net](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C).
  
## <a name="see-also"></a>Confira também

- [APIs exportadas do Outlook](outlook-exported-apis.md)
- [Constantes (Outlook exportados APIs)](constants-outlook-exported-apis.md)
- [Sobre APIs exportadas pelo Outlook](about-apis-exported-by-outlook.md)
- [Implementando coletores de eventos do Outlook 2002/XP no MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

