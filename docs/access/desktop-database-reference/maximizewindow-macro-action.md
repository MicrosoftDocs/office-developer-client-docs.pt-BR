---
title: Ação da macro MaximizarJanela
TOCTitle: MaximizeWindow macro action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 262e6781b61018cec3d52dbb930f380d3ff5bd85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289746"
---
# <a name="maximizewindow-macro-action"></a>Ação da macro MaximizarJanela

**Aplica-se ao:** Access 2013, Office 2013

Se o Access estiver configurado para usar janelas sobrepostas em vez de documentos com guias, você poderá usar a ação **MaximizeWindow** para ampliar a janela ativa para que ela preencha a janela do Access. Esta ação permitirá ver o máximo possível do objeto na janela ativa.

> [!NOTE]
> [!OBSERVAçãO] Essa ação não pode ser aplicada a janelas de código do Editor do Visual Basic (VBE). Para obter informações sobre como manipular janelas de código, consulte o tópico da propriedade **WindowState**.

## <a name="setting"></a>Setting

A ação **MaximizarJanela** não tem nenhum argumento.

## <a name="remarks"></a>Comentários

Esta ação equivale a clicar no botão **Maximizar** no canto superior direito ou clicar em **Maximizar** no menu **Controle** da janela.

Você pode usar a ação **RestaurarJanela** para restaurar uma janela maximizada para seu tamanho anterior.

> [!TIP]
> - Talvez seja necessário usar a ação **SelecionarObjeto** se a janela a ser maximizada não for a janela ativa.
> - Quando você maximizar uma janela no Access, todas as outras também serão maximizadas ao abri-las ou alternar para elas. Entretanto, os formulários pop-up não o serão. Se você desejar que um formulário mantenha o tamanho quando outras janelas forem maximizadas, defina a propriedade **PopUp** como **Sim**.

Para executar a ação **MaximizarJanela** em um módulo do Visual Basic for Applications, use o método **Maximizar** do objeto **DoCmd**.

