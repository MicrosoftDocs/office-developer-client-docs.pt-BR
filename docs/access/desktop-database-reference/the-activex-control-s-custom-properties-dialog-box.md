---
<<<<<<< Título cabeça: TOCTitle de caixa de diálogo do controle ActiveX personalizado propriedades: ms:assetid de caixa de diálogo de propriedades personalizadas do controle ActiveX: 124cf679-6efc-567a-84d1-8057dec93bde ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15) ms:contentKeyID: 48543338 MS.Date: 18/09/2015 === título: caixa de diálogo de propriedades personalizadas do ActiveX controle TOCTitle: Descrição da caixa de diálogo Propriedades personalizadas do ActiveX controle: esta caixa de diálogo de propriedades personalizadas oferece uma alternativa à lista de propriedades do Microsoft Access folha de propriedades para definir as propriedades do controle ActiveX no modo de Design.
MS:AssetID: 124cf679-6efc-567a-84d1-8057dec93bde ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15) ms:contentKeyID: ms.date 48543338: 10/16/2018
>>>>>>> mtps_version mestre: v=office.15 f1_keywords:
- vbaac10.chm4040 f1_categories:
- Office.Version=v15
---

<<<<<<< Cabeça
# <a name="activex-controls-custom-properties-dialog-box"></a>Caixa de diálogo de propriedades personalizadas do controle ActiveX
=======
# <a name="activex-control-custom-properties-dialog-box"></a>Caixa de diálogo de propriedades personalizadas de controle ActiveX
>>>>>>> mestre

**Aplica-se a**: Access 2013 | Office 2013

Durante a definição das propriedades de um controle ActiveX, pode ser que você precise ou prefira utilizar a caixa de diálogo de propriedades personalizadas do controle. Essa caixa de diálogo de propriedades personalizadas oferece uma alternativa à lista de propriedades da folha de propriedades do Microsoft Access para definir as propriedades dos controles ActiveX no modo de design.

> [!NOTE]
> [!OBSERVAçãO] Essas informações somente se aplicam aos controles ActiveX em um ambiente de banco de dados do Microsoft Access.

<<<<<<< Cabeça


## <a name="two-ways-to-set-properties"></a>Duas maneiras de definir propriedades
=======
## <a name="two-ways-to-set-properties"></a>Duas maneiras de definir propriedades
>>>>>>> mestre

A razão pela qual existe a caixa de diálogo de propriedades personalizadas é que nem todos os aplicativos que utilizam os controles ActiveX proporcionam uma folha de propriedades como aquela do Microsoft Access. A caixa de diálogo de propriedades personalizadas oferece uma interface para a definição das propriedades de controles-chave, independentemente da interface oferecida pelo aplicativo hospedeiro.

Para algumas propriedades de controles ActiveX, você pode optar por uma destas duas localizações para definir a propriedade:

<<<<<<< Cabeça
  - A folha de propriedades do Microsoft Access.

  - A caixa de diálogo de propriedades personalizadas do controle ActiveX.

Em alguns casos, a caixa de diálogo de propriedades personalizadas é a única maneira de definir uma propriedade no modo de design. Isto geralmente ocorre quando a interface precisa definir uma propriedade que não funciona dentro da folha de propriedades do Microsoft Access. Por exemplo, a propriedade **GridFont** para o Controle de Calendário tem muitos argumentos; você não pode definir mais de um argumento por propriedade na folha de propriedades do Microsoft Access.

## <a name="finding-the-custom-properties-dialog-box"></a>Localizando a caixa de diálogo de propriedades personalizadas

Nem todos os controles ActiveX proporcionam uma caixa de diálogo de propriedades personalizadas. Para ver se um controle oferece essa caixa de diálogo de propriedades personalizadas, procure pela propriedade **Personalizar** na folha de propriedades do Microsoft Access para esse controle. Se a lista de propriedades contiver o nome **Personalizar**, então o controle oferece a caixa de diálogo de propriedades personalizadas.

## <a name="using-the-custom-properties-dialog-box"></a>Utilizando a caixa de diálogo de propriedades personalizadas

Depois de clicar na caixa da propriedade **Personalizar** na folha de propriedades do Microsoft Access, clique no botão **Construir** à direita da caixa de propriedades para exibir a caixa de diálogo de propriedades personalizadas do controle, apresentada frequentemente como uma caixa de diálogo com guias. Escolha a guia que contém a interface para a configuração das propriedades que você deseja definir.

Após fazer as alterações em uma guia, em geral, é possível aplicar essas alterações clicando imediatamente no botão **Aplicar** (se fornecido). Você pode clicar em outras guias para definir outras propriedades, se necessário. Para aprovar todas as alterações feitas na caixa de diálogo de propriedades personalizadas, clique no botão **OK**. Para retornar à folha de propriedades do Microsoft Access sem alterar nenhuma definição de propriedade, clique no botão **Cancelar**.

Você também pode visualizar a caixa de diálogo de propriedades personalizadas clicando no subcomando **Propriedades** do comando **Objeto** do controle ActiveX (por exemplo, **Objeto Calendar Control**) no menu **Editar**, ou clicando nesse mesmo subcomando no menu de atalho do controle ActiveX. Além disso, algumas propriedades na folha de propriedades do Microsoft Access para o controle ActiveX, como a propriedade **GridFontColor** do Controle de Calendário, têm um botão **Construir** à direita da caixa de propriedades. Quando você clica no botão **Construir**, a caixa de diálogo de propriedades personalizadas é exibida, com a guia apropriada selecionada (por exemplo, **Cores**).
=======
- A folha de propriedades do Microsoft Access.
- A caixa de diálogo de propriedades personalizadas do controle ActiveX.

Em alguns casos, a caixa de diálogo de propriedades personalizadas é a única maneira de definir uma propriedade no modo de design. Isto geralmente ocorre quando a interface precisa definir uma propriedade que não funciona dentro da folha de propriedades do Microsoft Access. Por exemplo, a propriedade **GridFont** para o Controle de Calendário tem muitos argumentos; você não pode definir mais de um argumento por propriedade na folha de propriedades do Microsoft Access.

## <a name="finding-the-custom-properties-dialog-box"></a>Localizando a caixa de diálogo de propriedades personalizadas

Nem todos os controles ActiveX proporcionam uma caixa de diálogo de propriedades personalizadas. Para ver se um controle oferece essa caixa de diálogo de propriedades personalizadas, procure pela propriedade **Personalizar** na folha de propriedades do Microsoft Access para esse controle. Se a lista de propriedades contiver o nome **personalizado**, o controle fornece a caixa de diálogo de propriedades personalizadas.

## <a name="using-the-custom-properties-dialog-box"></a>Usando a caixa de diálogo de propriedades personalizadas

Depois que você escolher a caixa de propriedade **personalizada** na folha de propriedades do Microsoft Access, escolha o botão **Construir** , à direita da caixa de propriedade para exibir a caixa de diálogo de propriedades personalizadas do controle, apresentada frequentemente como uma caixa de diálogo com guias. Escolha a guia que contém a interface para a configuração das propriedades que você deseja definir.

Depois de fazer alterações em uma guia, você pode frequentemente aplicar essas alterações imediatamente, escolhendo o botão **Aplicar** (se fornecido). Você pode escolher outras guias para definir outras propriedades conforme necessário. Para aprovar todas as alterações feitas na caixa de diálogo de propriedades personalizadas, escolha o botão de **Okey** . Para retornar à folha de propriedade do Microsoft Access sem alterar as configurações de propriedade, escolha o botão **Cancelar** .

Também é possível exibir a caixa de diálogo de propriedades personalizadas, escolhendo o subcomando de **Propriedades** do controle ActiveX do comando (por exemplo, o **Objeto de controle de calendário**) do **objeto** no menu **Editar** , ou escolhendo nesse mesmo subcomando no o menu de atalho para o controle ActiveX. Além disso, algumas propriedades na folha de propriedades do Microsoft Access para o controle ActiveX, como a propriedade **GridFontColor** do Calendar Control, têm um botão **Construir** à direita da caixa de propriedades. Quando você escolhe o botão **Construir** , a caixa de diálogo de propriedades personalizadas é exibida, com a guia apropriada selecionada (por exemplo, **cores**).
>>>>>>> mestre

