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
# <a name="setproperty-macro-action"></a>Ação da macro DefinirPropriedade

**Aplica-se ao:** Access 2013, Office 2013

Você pode usar a ação **DefinirPropriedade** para definir uma propriedade para um controle em um formulário ou relatório.

## <a name="setting"></a>Configuração

A ação **DefinirPropriedade** tem os seguintes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento da ação</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Nome do controle</p></td>
<td><p>Digite o nome do campo ou do controle para o qual você deseja definir o valor da propriedade. Use somente o nome do controle, e não a sintaxe completa. Deixe este argumento em branco para definir a propriedade do formulário ou do relatório atual.</p></td>
</tr>
<tr class="even">
<td><p>Propriedade	</p></td>
<td><p>Selecione a propriedade a ser definida. Consulte a seção <strong>Comentários</strong> deste artigo para obter uma lista das propriedades que podem ser definidas com esta ação.</p></td>
</tr>
<tr class="odd">
<td><p>Valor</p></td>
<td><p>Digite o valor com o qual a propriedade deve ser definida. Para propriedades cujos valores sejam Sim ou Não, use <strong>-1</strong> para Sim e <strong>0</strong> para Não.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

- Você pode usar a ação **DefinirPropriedade** para definir estas propriedades de um controle: **Habilitado**, **Visível**, **Locked**, **Esquerdo**, **Superior**, **Largura**, **Altura**, **Cor de Primeiro Plano**, **Cor do Fundo** ou **Legenda**.

- Se você inserir um valor inválido para o argumento ***Valor***, não ocorrerá nenhum erro, mas o Access poderá alterar a propriedade para um valor diferente, dependendo da forma como o Access interpretar o argumento.

- A ação **DefinirPropriedade** poderá ser usada em uma macro autônoma somente se você precedê-la com uma ação que selecione o formulário ou o relatório contendo o controle para o qual está definindo a propriedade. Se o formulário ou o relatório não estiver aberto, você poderá usar a ação **AbrirFormulário** ou a ação **AbrirRelatório** para abri-lo ou selecioná-lo. Se o formulário ou o relatório já estiver aberto, use a ação **SelecionarObjeto** para selecioná-lo. Depois use a ação **DefinirPropriedade** para definir a propriedade. A seleção do objeto não será necessária se você usar a ação **DefinirPropriedade** em uma macro que esteja inserida em um controle do mesmo formulário ou relatório como o controle para o qual você está definindo a propriedade.

- Para executar a ação **DefinirPropriedade** em um módulo do VBA, use o método **SetProperty** do objeto **DoCmd**.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra como usar a ação setProperty para alternar a visibilidade da caixa **** de texto myTextBox.

**Código de exemplo fornecido por:** a [Referência do programador do Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
