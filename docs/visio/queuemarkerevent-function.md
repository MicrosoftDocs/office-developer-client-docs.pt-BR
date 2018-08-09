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
description: Faz com que o aplicativo emita um evento de marcador no seu complemento, o Microsoft Visual Basic for Applications (VBA) código ou suplemento COM.
ms.openlocfilehash: b9175caf0845530c93f6db15e286f3eae21ea415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772626"
---
# <a name="queuemarkerevent-function"></a>Função QUEUEMARKEREVENT

Faz com que o aplicativo emita um evento de marcador no seu complemento, o Microsoft Visual Basic for Applications (VBA) código ou suplemento COM. 
  
## <a name="syntax"></a>Sintaxe

QUEUEMARKEREVENT (* * *event_string* * *) 
  
### <a name="parameters"></a>Parâmetros

|**Name**|**Obrigatório/Opcional**|**Tipo de dados**|**Descrição**|
|:-----|:-----|:-----|:-----|
| _event_string_ <br/> |Obrigatório  <br/> |**String** <br/> | A cadeia de caracteres a serem passados para o manipulador de eventos.  <br/> |
   
## <a name="remarks"></a>Comentários

A função QUEUEMARKEREVENT fornece aos desenvolvedores uma maneira para notificar o código de uma célula ShapeSheet e passar informações específicas da solução. Quando a célula que contém a fórmula com a função QUEUEMARKEREVENT é avaliada, o aplicativo dispara um evento de marcador e passa _event_string_ para todos os manipuladores de eventos que estejam escutando o evento **MarkerEvent** . 
  
Para obter mais informações sobre eventos de marcadores, consulte o método **QueueMarkerEvent** e o **evento MarkerEvent na referência de automação do Microsoft Visio** . 
  
## <a name="example"></a>Exemplo

QUEUEMARKEREVENT ("MinhaNotificaçãoPersonalizada") 
  
Faz com que o aplicativo emita um evento de marcador e passe a sequência de caracteres "MinhaNotificaçãoPersonalizada" para manipuladores de eventos que estejam escutando o evento **MarkerEvent**. 
  

