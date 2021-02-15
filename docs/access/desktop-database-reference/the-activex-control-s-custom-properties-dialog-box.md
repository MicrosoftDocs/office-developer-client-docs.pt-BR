---
title: Caixa de diálogo propriedades personalizadas do controle ActiveX
TOCTitle: ActiveX control custom properties dialog box
description: Essa caixa de diálogo de propriedades personalizadas proporciona uma alternativa à lista de propriedades da folha de propriedades do Microsoft Access para definir as propriedades dos controles ActiveX no modo de design.
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4574abc86e6eacd38721e601d26c8b8fbf0a0d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314102"
---
# <a name="activex-control-custom-properties-dialog-box"></a>Caixa de diálogo propriedades personalizadas do controle ActiveX

**Aplica-se ao:** Access 2013, Office 2013

Durante a definição das propriedades de um controle ActiveX, pode ser que você precise ou prefira utilizar a caixa de diálogo de propriedades personalizadas do controle. Essa caixa de diálogo de propriedades personalizadas oferece uma alternativa à lista de propriedades da folha de propriedades do Microsoft Access para definir as propriedades dos controles ActiveX no modo de design.

> [!NOTE]
> [!OBSERVAçãO] Essas informações somente se aplicam aos controles ActiveX em um ambiente de banco de dados do Microsoft Access.

## <a name="two-ways-to-set-properties"></a>Duas maneiras de definir propriedades

A razão pela qual existe a caixa de diálogo de propriedades personalizadas é que nem todos os aplicativos que utilizam os controles ActiveX proporcionam uma folha de propriedades como aquela do Microsoft Access. A caixa de diálogo de propriedades personalizadas oferece uma interface para a definição das propriedades de controles-chave, independentemente da interface oferecida pelo aplicativo hospedeiro.

Para algumas propriedades de controles ActiveX, você pode optar por uma destas duas localizações para definir a propriedade:

- A folha de propriedades do Microsoft Access.
- A caixa de diálogo de propriedades personalizadas do controle ActiveX.

Em alguns casos, a caixa de diálogo de propriedades personalizadas é a única maneira de definir uma propriedade no modo de design. Isto geralmente ocorre quando a interface precisa definir uma propriedade que não funciona dentro da folha de propriedades do Microsoft Access. Por exemplo, a propriedade **GridFont** para o Controle de Calendário tem muitos argumentos; você não pode definir mais de um argumento por propriedade na folha de propriedades do Microsoft Access.

## <a name="finding-the-custom-properties-dialog-box"></a>Localizar a caixa de diálogo de propriedades personalizadas

Nem todos os controles ActiveX proporcionam uma caixa de diálogo de propriedades personalizadas. Para ver se um controle oferece essa caixa de diálogo de propriedades personalizadas, procure pela propriedade **Personalizar** na folha de propriedades do Microsoft Access para esse controle. Se a lista de propriedades contiver o nome **Personalizado**, o controle fornece a caixa de diálogo de propriedades personalizadas.

## <a name="using-the-custom-properties-dialog-box"></a>Usando a caixa de diálogo de propriedades personalizadas

Depois de  escolher a caixa de propriedades Personalizada  na folha de propriedades do Microsoft Access, escolha o botão Construir à direita da caixa de propriedades para exibir a caixa de diálogo de propriedades personalizadas do controle, geralmente apresentada como uma caixa de diálogo com guias. Escolha a guia que contém a interface para definir as propriedades que você deseja definir.

Depois de fazer alterações em uma guia, geralmente você pode aplicar essas alterações imediatamente escolhendo o botão **Aplicar** (se fornecido). Você pode escolher outras guias para definir outras propriedades conforme necessário. Para aprovar todas as alterações feitas na caixa de diálogo de propriedades personalizadas, escolha o **botão OK.** Para retornar à folha de propriedades do Microsoft Access sem alterar nenhuma configuração de propriedade, escolha o **botão** Cancelar.

Você também pode exibir a caixa de diálogo de propriedades personalizadas  escolhendo o **subcomando** Propriedades do comando Objeto do controle ActiveX (por **exemplo,** Objeto de Controle de Calendário) no **menu** Editar ou escolhendo esse mesmo subcomando no menu de atalho do controle ActiveX. Além disso, algumas propriedades na folha de propriedades do Microsoft Access para o controle ActiveX, como a propriedade **GridFontColor** do Calendar Control, têm um botão **Construir** à direita da caixa de propriedades. Quando você escolhe o **botão Construir,** a caixa de diálogo de propriedades personalizadas é exibida, com a guia apropriada selecionada (por exemplo, **Cores**).

