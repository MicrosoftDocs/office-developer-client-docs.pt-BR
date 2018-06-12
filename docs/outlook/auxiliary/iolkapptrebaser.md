---
title: IOlkApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d67bd395-d324-217d-8ddc-1d48dd724383
description: Suporta a alteração da Base de compromissos em uma pasta de calendário.
ms.openlocfilehash: 57ca59121f74c7b64a84282c7493e4aed3179f7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765984"
---
# <a name="iolkapptrebaser"></a>IOlkApptRebaser

Suporta a alteração da Base de compromissos em uma pasta de calendário.
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Herda de:  <br/> |**IUnknown** <br/> |
|Arquivo de cabeçalho:  <br/> |tzmovelib.h  <br/> |
|Implementada por:  <br/> |tzmovelib.dll  <br/> |
|Chamado pelo:  <br/> |Aplicativos de cliente MAPI  <br/> |
|Expostas no:  <br/> |REBASE de objeto do Outlook  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|**[BeginEnumerateAppointments](iolkapptrebaser-beginenumerateappointments.md)** <br/> |Inicia uma tarefa a enumeração de compromisso em uma pasta de calendário para encontrar os compromissos que precisam a alteração da base.  <br/> |
|**[EndEnumerateAppointments](iolkapptrebaser-endenumerateappointments.md)** <br/> |Aguardará enumeração de compromisso em uma pasta de calendário para a conclusão e retorna uma lista de compromissos essa necessidade alteração da base.  <br/> |
|**[BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md)** <br/> |Inicia uma tarefa a alteração da compromisso base fornecida uma lista de compromissos, normalmente obtido da **EndEnumerateAppointments**.  <br/> |
|**[EndRebaseAppointments](iolkapptrebaser-endrebaseappointments.md)** <br/> |Aguardará compromisso a alteração da base para concluir e recupera os resultados.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Sobre alteração de calendários por meio de programação para horário de verão](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

