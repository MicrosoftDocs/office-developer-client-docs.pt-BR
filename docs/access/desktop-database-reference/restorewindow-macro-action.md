---
title: Ação da macro RestaurarJanela
TOCTitle: RestoreWindow macro action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 35637781035b7a449ba574cf5f6c84f2cb5223db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306584"
---
# <a name="restorewindow-macro-action"></a>Ação da macro RestaurarJanela

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **RestaurarJanela** para restaurar uma janela maximizada ou minimizada ao seu tamanho anterior.

> [!NOTE]
> [!OBSERVAçãO] Essa ação não pode ser aplicada a janelas de código do Editor do Visual Basic (VBE). Para obter informações sobre como manipular janelas de código, consulte o tópico da propriedade **WindowState**.

## <a name="setting"></a>Setting

A ação **RestaurarJanela** não tem argumentos.

## <a name="remarks"></a>Comentários

Essa ação abrange o objeto selecionado. Se um objeto for minimizado, você poderá primeiro selecioná-lo usando a ação **SelecionarObjeto** e então restaurá-lo ao tamanho anterior usando a ação **RestaurarJanela**.

Também é possível usar a ação **MovereDimensionarJanela** para mover ou dimensionar uma janela restaurada.

A ação **RestaurarJanela** tem o mesmo efeito de clicar no botão **Restaurar**, localizado no canto superior direito da janela, ou de clicar no comando **Restaurar**, localizado no menu **Controle** da janela.

Para executar a ação **RestaurarJanela** em um módulo do VBA (Visual Basic for Applications), use o método **Restaurar** do objeto **DoCmd**.

