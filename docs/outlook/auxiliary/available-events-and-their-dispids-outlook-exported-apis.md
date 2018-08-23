---
title: Eventos disponíveis e os dispids (Outlook exportados APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: Esta seção descreve os identificadores de expedição para os eventos que disponibiliza Outlook.
ms.openlocfilehash: a94787063e0fd5be30de1ef772813979d3cb2f21
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582970"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Eventos disponíveis e os dispids (Outlook exportados APIs)

Esta seção descreve os identificadores de expedição para os eventos que disponibiliza Outlook.
  
Outlook expõe os seguintes identificadores de expedição (dispids) para permitir que os suplementos de C++ ouvir e manipular os eventos correspondentes da função [IDispatch:: Invoke](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) . 
  
|**Constante**|**DISPID de evento**|**Descrição**|**Parameters**|**Comentários**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Usado para manipular o evento de nível de aplicativo da função **IDispatch:: Invoke** que é acionado antes de uma operação de impressão.  <br/> | Há 2 parâmetros sem nome:  <br/>  O primeiro parâmetro é do tipo * * VT_BOOL|VT_BREF * *. Retorne **VARIANT_TRUE** neste parâmetro para cancelar o evento.  <br/>  O segundo parâmetro não for usado e deve ser ignorado.  <br/> |Este dispid está disponível desde o Outlook 2010.  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Usado para manipular o evento de nível de item da função **IDispatch:: Invoke** que é acionado quando o Outlook concluiu a ler as propriedades do item.  <br/> |Há apenas um parâmetro _Cancelar_ que é do tipo * * VT_BOOL|VT_BREF * *. Retorne **VARIANT_TRUE** neste parâmetro para cancelar a operação de leitura.  <br/> |Este dispid está disponível desde o Outlook 2010.  <br/> Esse evento corresponde ao evento do Exchange Client ECE (extensões) **IExchExtMessageEvents::OnReadComplete**e também ao evento **ReadComplete** que foi adicionada ao modelo de objeto desde o Outlook 2013.  <br/> |
   
Para obter um exemplo de como usar um dispid ouvir e manipular um evento, consulte o `CAppEventListener::Invoke` função na solução C++ Outlook descrita em [Implementando o Coletores de eventos do Outlook 2002/XP no MFC C++ 2003 .NET](http://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C).
  
## <a name="see-also"></a>Confira também

- [APIs exportadas do Outlook](outlook-exported-apis.md)
- [Constantes (Outlook exportados APIs)](constants-outlook-exported-apis.md)
- [Sobre APIs exportadas pelo Outlook](about-apis-exported-by-outlook.md)
- [Implementar o Outlook 2002/XP evento recpetores no .NET 2003 do C++ MFC](http://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

