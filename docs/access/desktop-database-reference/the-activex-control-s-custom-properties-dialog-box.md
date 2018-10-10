---
title: Caixa de diálogo de propriedades personalizadas do controle ActiveX
TOCTitle: ActiveX Control's Custom Properties Dialog Box
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6f5924d04e9ea4febee1434f6ef99f95b02eab6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463969"
---
# <a name="activex-controls-custom-properties-dialog-box"></a>Caixa de diálogo de propriedades personalizadas do controle ActiveX

**Aplica-se a**: Access 2013 | Office 2013

Durante a definição das propriedades de um controle ActiveX, pode ser que você precise ou prefira utilizar a caixa de diálogo de propriedades personalizadas do controle. Essa caixa de diálogo de propriedades personalizadas oferece uma alternativa à lista de propriedades da folha de propriedades do Microsoft Access para definir as propriedades dos controles ActiveX no modo de design.

> [!NOTE]
> [!OBSERVAçãO] Essas informações somente se aplicam aos controles ActiveX em um ambiente de banco de dados do Microsoft Access.



## <a name="two-ways-to-set-properties"></a>Duas maneiras de definir propriedades

A razão pela qual existe a caixa de diálogo de propriedades personalizadas é que nem todos os aplicativos que utilizam os controles ActiveX proporcionam uma folha de propriedades como aquela do Microsoft Access. A caixa de diálogo de propriedades personalizadas oferece uma interface para a definição das propriedades de controles-chave, independentemente da interface oferecida pelo aplicativo hospedeiro.

Para algumas propriedades de controles ActiveX, você pode optar por uma destas duas localizações para definir a propriedade:

  - A folha de propriedades do Microsoft Access.

  - A caixa de diálogo de propriedades personalizadas do controle ActiveX.

Em alguns casos, a caixa de diálogo de propriedades personalizadas é a única maneira de definir uma propriedade no modo de design. Isto geralmente ocorre quando a interface precisa definir uma propriedade que não funciona dentro da folha de propriedades do Microsoft Access. Por exemplo, a propriedade **GridFont** para o Controle de Calendário tem muitos argumentos; você não pode definir mais de um argumento por propriedade na folha de propriedades do Microsoft Access.

## <a name="finding-the-custom-properties-dialog-box"></a>Localizando a caixa de diálogo de propriedades personalizadas

Nem todos os controles ActiveX proporcionam uma caixa de diálogo de propriedades personalizadas. Para ver se um controle oferece essa caixa de diálogo de propriedades personalizadas, procure pela propriedade **Personalizar** na folha de propriedades do Microsoft Access para esse controle. Se a lista de propriedades contiver o nome **Personalizar**, então o controle oferece a caixa de diálogo de propriedades personalizadas.

## <a name="using-the-custom-properties-dialog-box"></a>Utilizando a caixa de diálogo de propriedades personalizadas

Depois de clicar na caixa da propriedade **Personalizar** na folha de propriedades do Microsoft Access, clique no botão **Construir** à direita da caixa de propriedades para exibir a caixa de diálogo de propriedades personalizadas do controle, apresentada frequentemente como uma caixa de diálogo com guias. Escolha a guia que contém a interface para a configuração das propriedades que você deseja definir.

Após fazer as alterações em uma guia, em geral, é possível aplicar essas alterações clicando imediatamente no botão **Aplicar** (se fornecido). Você pode clicar em outras guias para definir outras propriedades, se necessário. Para aprovar todas as alterações feitas na caixa de diálogo de propriedades personalizadas, clique no botão **OK**. Para retornar à folha de propriedades do Microsoft Access sem alterar nenhuma definição de propriedade, clique no botão **Cancelar**.

Você também pode visualizar a caixa de diálogo de propriedades personalizadas clicando no subcomando **Propriedades** do comando **Objeto** do controle ActiveX (por exemplo, **Objeto Calendar Control**) no menu **Editar**, ou clicando nesse mesmo subcomando no menu de atalho do controle ActiveX. Além disso, algumas propriedades na folha de propriedades do Microsoft Access para o controle ActiveX, como a propriedade **GridFontColor** do Controle de Calendário, têm um botão **Construir** à direita da caixa de propriedades. Quando você clica no botão **Construir**, a caixa de diálogo de propriedades personalizadas é exibida, com a guia apropriada selecionada (por exemplo, **Cores**).

