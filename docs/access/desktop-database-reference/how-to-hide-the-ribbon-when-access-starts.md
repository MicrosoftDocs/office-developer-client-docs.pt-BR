---
title: Ocultar a faixa de opções quando o Access for iniciado
TOCTitle: Hide the ribbon when Access starts
description: Como carregar uma faixa de opções personalizada que oculta todas as guias internas no Access 2013.
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
ms.openlocfilehash: 21c8a171a3b84e53f5a12042a09b134602a6af6f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875312"
---
# <a name="hide-the-ribbon-when-access-starts"></a>Ocultar a faixa de opções quando o Access for iniciado

**Aplica-se a:** Access 2013 | Office 2013

Por padrão, o Microsoft Access não oferece um método para ocultar a faixa de opções. Este tópico descreve como carregar uma faixa de opções personalizada que oculta todas as guias internas.

Para carregar a faixa de opções personalizada quando o Access for iniciado, você deverá armazenar suas configurações em uma tabela chamada **USysRibbons**.

A tabela **USysRibbons** deve ser criada com o uso de nomes de coluna específica para as personalizações de faixa de opções a serem implementadas. 

A tabela a seguir lista as configurações a serem usadas na criação da tabela **USysRibbons**.

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
<td><p>Contém a extensibilidade da faixa de opções XML (RibbonX) que define a personalização da faixa de opções.</p></td>
</tr>
</tbody>
</table>

<br/>

A tabela a seguir lista as configurações de personalização da faixa de opções a serem armazenadas na tabela **USysRibbons**.

|Nome da coluna|Valor|
|:----------|:----|
|**RibbonName**|HideTheRibbon|
|**RibbonXML**|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a>Aplicar uma faixa de opções personalizada ao iniciar o Access

Para aplicar uma faixa de opções personalizada de forma que ela esteja disponível quando o aplicativo for iniciado, use o seguinte procedimento:

1.  Siga o processo descrito anteriormente para disponibilizar a faixa de opções personalizada para o aplicativo.

2.  Feche e então reinicie o aplicativo.

3.  Escolha o **Botão do Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102")e escolha **Opções do Access**.

4.  Escolha a opção de **Banco de dados atual** e em seguida, na seção **Opções de barra de ferramentas e faixa de opções** , escolha a lista **Nome da faixa de opções** e selecione **HideTheRibbon**.

5.  Feche e então reinicie o aplicativo.

> [!NOTE]
> [!OBSERVAçãO] Para saber mais sobre a interface do usuário da faixa de opções em outros aplicativos do Office, consulte [Visão geral da faixa de opções do Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


