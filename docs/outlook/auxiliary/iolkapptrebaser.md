---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: O suporta a alteração da base dos compromissos em uma pasta de calendário.
ms.openlocfilehash: cf4f7c790a8561f149160c83418a0d5ebd91a455
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410067"
---
# <a name="iolkapptrebaser"></a>IOlkApptRebaser

O suporta a alteração da base dos compromissos em uma pasta de calendário.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |**IUnknown** <br/> |
|Arquivo de cabeçalho:  <br/> |tzmovelib.h  <br/> |
|Implementado por:  <br/> |tzmovelib.dll  <br/> |
|Chamado por:  <br/> |Aplicativos clientes MAPI  <br/> |
|Exposto em:  <br/> |Objeto rebasing do Outlook  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)** <br/> |Inicia uma tarefa para enumeração de compromisso em uma pasta de calendário para localizar os compromissos que precisam de alteração de base.  <br/> |
|**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)** <br/> |Aguarda a conclusão da enumeração de compromissos em uma pasta de calendário e retorna uma lista de compromissos que precisam de alteração programática.  <br/> |
|**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)** <br/> |Inicia uma tarefa para a alteração da base de compromisso, dada uma lista de compromissos, geralmente Obtida de **EndEnumerateAppointments**.  <br/> |
|**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)** <br/> |Aguarda a alteração da base do compromisso para concluir e recupera os resultados.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Sobre a alteração programática da base de calendários para o horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

