---
title: Ação da macro DefinirPropriedade
TOCTitle: SetProperty macro action
ms:assetid: 58d2eac3-35b2-e9f8-47e0-62c9b52f2c24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194340(v=office.15)
ms:contentKeyID: 48545004
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm139044
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c5972ad630efe3afe27565924c7c6a8a2230a9f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314571"
---
# <a name="setproperty-macro-action"></a><span data-ttu-id="4b97a-102">Ação da macro DefinirPropriedade</span><span class="sxs-lookup"><span data-stu-id="4b97a-102">SetProperty macro action</span></span>

<span data-ttu-id="4b97a-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b97a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b97a-104">Você pode usar a ação **DefinirPropriedade** para definir uma propriedade para um controle em um formulário ou relatório.</span><span class="sxs-lookup"><span data-stu-id="4b97a-104">You can use the **SetProperty** action to set a property for a control on a form or a report.</span></span>

## <a name="setting"></a><span data-ttu-id="4b97a-105">Configuração</span><span class="sxs-lookup"><span data-stu-id="4b97a-105">Setting</span></span>

<span data-ttu-id="4b97a-106">A ação **DefinirPropriedade** tem os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="4b97a-106">The **SetProperty** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b97a-107">Argumento da ação</span><span class="sxs-lookup"><span data-stu-id="4b97a-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4b97a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b97a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b97a-109">Nome do controle</span><span class="sxs-lookup"><span data-stu-id="4b97a-109">Control Name</span></span></p></td>
<td><p><span data-ttu-id="4b97a-110">Digite o nome do campo ou do controle para o qual você deseja definir o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="4b97a-110">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="4b97a-111">Use somente o nome do controle, e não a sintaxe completa.</span><span class="sxs-lookup"><span data-stu-id="4b97a-111">Use only the control name, not the full syntax.</span></span> <span data-ttu-id="4b97a-112">Deixe este argumento em branco para definir a propriedade do formulário ou do relatório atual.</span><span class="sxs-lookup"><span data-stu-id="4b97a-112">Leave this argument blank to set the property for the current form or report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b97a-113">Propriedade	</span><span class="sxs-lookup"><span data-stu-id="4b97a-113">Property</span></span></p></td>
<td><p><span data-ttu-id="4b97a-p102">Selecione a propriedade a ser definida. Consulte a seção <strong>Comentários</strong> deste artigo para obter uma lista das propriedades que podem ser definidas com esta ação.</span><span class="sxs-lookup"><span data-stu-id="4b97a-p102">Select the property that you want to set. See the <strong>Remarks</strong> section in this article for a list of the properties that can be set by using this action.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b97a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="4b97a-116">Value</span></span></p></td>
<td><p><span data-ttu-id="4b97a-p103">Digite o valor com o qual a propriedade deve ser definida. Para propriedades cujos valores sejam Sim ou Não, use <strong>-1</strong> para Sim e <strong>0</strong> para Não.</span><span class="sxs-lookup"><span data-stu-id="4b97a-p103">Type the value that the property is to be set to. For properties whose values are either Yes or No, use <strong>-1</strong> for Yes and <strong>0</strong> for No.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4b97a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b97a-119">Remarks</span></span>

- <span data-ttu-id="4b97a-120">Você pode usar a ação **DefinirPropriedade** para definir estas propriedades de um controle: **Habilitado**, **Visível**, **Locked**, **Esquerdo**, **Superior**, **Largura**, **Altura**, **Cor de Primeiro Plano**, **Cor do Fundo** ou **Legenda**.</span><span class="sxs-lookup"><span data-stu-id="4b97a-120">You can use the **SetProperty** action to set the following properties of a control: **Enabled**, **Visible**, **Locked**, **Left**, **Top**, **Width**, **Height**, **Fore Color**, **Back Color**, or **Caption**.</span></span>

- <span data-ttu-id="4b97a-121">Se você inserir um valor inválido para o argumento ***Valor***, não ocorrerá nenhum erro, mas o Access poderá alterar a propriedade para um valor diferente, dependendo da forma como o Access interpretar o argumento.</span><span class="sxs-lookup"><span data-stu-id="4b97a-121">If you enter an invalid value for the ***Value*** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span>

- <span data-ttu-id="4b97a-p104">A ação **DefinirPropriedade** poderá ser usada em uma macro autônoma somente se você precedê-la com uma ação que selecione o formulário ou o relatório contendo o controle para o qual está definindo a propriedade. Se o formulário ou o relatório não estiver aberto, você poderá usar a ação **AbrirFormulário** ou a ação **AbrirRelatório** para abri-lo ou selecioná-lo. Se o formulário ou o relatório já estiver aberto, use a ação **SelecionarObjeto** para selecioná-lo. Depois use a ação **DefinirPropriedade** para definir a propriedade. A seleção do objeto não será necessária se você usar a ação **DefinirPropriedade** em uma macro que esteja inserida em um controle do mesmo formulário ou relatório como o controle para o qual você está definindo a propriedade.</span><span class="sxs-lookup"><span data-stu-id="4b97a-p104">You can use the **SetProperty** action in a stand-alone macro only if you precede it with an action that selects the form or report containing the control for which you are setting the property. If the form or report is not open, you can use the **OpenForm** or **OpenReport** action to open and select it. If the form or report is already open, you can use the **SelectObject** action to select it. You can then use the **SetProperty** action to set the property. Selecting the object is not necessary if you use the **SetProperty** action in a macro which is embedded in a control on the same form or report as the control for which you are setting the property.</span></span>

- <span data-ttu-id="4b97a-127">Para executar a ação **DefinirPropriedade** em um módulo do VBA, use o método **SetProperty** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="4b97a-127">To run the **SetProperty** action in a VBA module, use the **SetProperty** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="4b97a-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4b97a-128">Example</span></span>

<span data-ttu-id="4b97a-129">O exemplo a seguir mostra como usar a ação setProperty para alternar a visibilidade da caixa \*\*\*\* de texto myTextBox.</span><span class="sxs-lookup"><span data-stu-id="4b97a-129">The following example shows how to use the SetProperty action to toggle the visibility of the **MyTextBox** text box.</span></span>

<span data-ttu-id="4b97a-130">**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="4b97a-130">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
