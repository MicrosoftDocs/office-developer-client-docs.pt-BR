---
title: Ocultar a faixa de opções quando o Access for iniciado
TOCTitle: Hide the ribbon when Access starts
description: Este tópico descreve como carregar uma faixa de opções personalizada que oculta todas as guias internas no Access 2013.
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 384a575ae5e15b75ba7b0b891529c695cc3de599
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537826"
---
# <a name="hide-the-ribbon-when-access-starts"></a>Ocultar a faixa de opções quando o Access for iniciado

**Aplica-se ao:** Access 2013 | Office 2013

Por padrão, o Microsoft Access não oferece um método para ocultar a faixa de opções. Este tópico descreve como carregar uma faixa de opções personalizada que oculta todas as guias internas.

Para carregar a faixa de opções personalizada quando o Access for iniciado, você deverá armazenar suas configurações em uma tabela chamada **USysRibbons**.

A tabela **USysRibbons** deve ser criada usando nomes de coluna específicos para que as personalizações da faixa de opções sejam implementadas. 

A tabela a seguir lista as configurações para usar ao criar a tabela **USysRibbons**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da coluna</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>Texto</p></td>
<td><p>Contém o nome da faixa de opções personalizada a ser associado à esta personalização.</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Memorando</p></td>
<td><p>Contém o XML de extensibilidade da Faixa de Opções (RibbonX) que define a personalização da faixa de opções.</p></td>
</tr>
</tbody>
</table>

<br/>

A tabela a seguir lista as configurações de personalização da faixa de opções a ser armazenada na tabela **USysRibbons**.

|Nome da coluna|Valor|
|:----------|:----|
|**RibbonName**|HideTheRibbon|
|**RibbonXML**|`<CustomUI xmlns="http://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a>Aplicar uma faixa de opções personalizada quando o Access iniciar

Para aplicar uma faixa de opções personalizada de forma que ela esteja disponível quando o aplicativo for iniciado, use o seguinte procedimento:

1.  Siga o processo descrito anteriormente para disponibilizar a faixa de opções personalizada para o aplicativo.

2.  Feche e então reinicie o aplicativo.

3.  Escolha o **Botão Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102"), e escolha **Opções de Acesso**.

4.  Escolha a opção **Banco de Dados Atual** e, em seguida, na seção **Opções da Faixa de Opções e da Barra de Ferramentas**, escolha a lista **Nome da Faixa de Opções** e selecione **HideTheRibbon**.

5.  Feche e então reinicie o aplicativo.

> [!NOTE]
> Para saber mais sobre a interface do usuário da faixa de opções em outros aplicativos do Office, consulte [Visão geral da faixa de opções do Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


