---
title: Função QUEUEMARKEREVENT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60107
localization_priority: Normal
ms.assetid: b4671715-4209-7774-c174-c19dc9721a02
description: Faz com que o aplicativo acione um evento de marcador no complemento, no código do Microsoft Visual Basic for Applications (VBA) ou no complemento COM.
ms.openlocfilehash: 841f6acc63497a6f0b8930c89534b5f8b04c0393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418803"
---
# <a name="queuemarkerevent-function"></a>Função QUEUEMARKEREVENT

Faz com que o aplicativo acione um evento de marcador no complemento, no código do Microsoft Visual Basic for Applications (VBA) ou no complemento COM. 
  
## <a name="syntax"></a>Sintaxe

QUEUEMARKEREVENT (** *event_string* ** ) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |Obrigatório  <br/> |**String** <br/> | A cadeia de caracteres a ser aprovada para o manipulador de eventos.  <br/> |
   
## <a name="remarks"></a>Comentários

A função QUEUEMARKEREVENT fornece aos desenvolvedores uma maneira de notificar o código de uma célula da ShapeSheet e passar informações específicas da solução. Quando a célula que contém a fórmula com a função QUEUEMARKEREVENT é avaliada, o aplicativo dispara um evento de marcador e passa _event_string_ para todos os manipuladores de eventos que estão escutando o evento **MarkerEvent.** 
  
Para obter mais informações sobre eventos de marcador, consulte os tópicos sobre o método **QueueMarkerEvent** e o evento **MarkerEvent** na Referência de Automação do Microsoft Visio. 
  
## <a name="example"></a>Exemplo

QUEUEMARKEREVENT ("MinhaNotificaçãoPersonalizada") 
  
Faz com que o aplicativo emita um evento de marcador e passe a sequência de caracteres "MinhaNotificaçãoPersonalizada" para manipuladores de eventos que estejam escutando o evento **MarkerEvent**. 
  

