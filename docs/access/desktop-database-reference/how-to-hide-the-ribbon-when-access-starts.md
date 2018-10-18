---
título: ocultar a faixa de opções ao iniciar o Access TOCTitle: ocultar a faixa de opções ao iniciar o Access <<<<<<< ms:assetid cabeça: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: ms.date 48548817: 18/09/2015 === Descrição: como carregar uma faixa de opções personalizada que oculta todas as guias internas no Access 2013.
MS:AssetID: f98bab58-8094-1c56-f70b-ced2e7849574 ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15) ms:contentKeyID: ms.date 48548817: 10/16/2018
>>>>>>> mtps_version mestre: v=office.15
---

# <a name="hide-the-ribbon-when-access-starts"></a>Ocultar a faixa de opções ao iniciar o Access

**Aplica-se a:** Access 2013 | Office 2013

Por padrão, o Microsoft Access não oferece um método para ocultar a faixa de opções. Este tópico descreve como carregar uma faixa de opções personalizada que oculta todas as guias internas.

Para carregar a faixa de opções personalizada quando o Access for iniciado, você deverá armazenar suas configurações em uma tabela chamada **USysRibbons**.

<<<<<<< Cabeça tabela **USysRibbons** deve ser criada usando nomes de coluna específica na ordem para as personalizações de faixa de opções a serem implementadas. A tabela a seguir lista as configurações a serem usadas na criação da tabela **USysRibbons**.
=== Tabela **USysRibbons** deve ser criada com o uso de nomes de coluna específica para as personalizações de faixa de opções a serem implementadas. 

A tabela a seguir lista as configurações a serem usadas na criação da tabela **USysRibbons**.
>>>>>>> mestre

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<<<<<<< Cabeça
<th><p>Nome da coluna</p></th>
<th><p>Tipo de dados</p></th>
=======
<th><p>Nome da coluna</p></th>
<th><p>Tipo de dados</p></th>
>>>>>>>mestre
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
<<<<<<< Cabeça
<td><p>Contém o XML de Extensibilidade da Faixa de Opções (RibbonX) que define a personalização da faixa de opções.</p></td>
=======
<td><p>Contém a extensibilidade da faixa de opções XML (RibbonX) que define a personalização da faixa de opções.</p></td>
>>>>>>>mestre
</tr>
</tbody>
</table>

<<<<<<< Cabeça

A tabela a seguir lista as configurações de personalização da faixa de opções a serem armazenadas na tabela **USysRibbons**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da coluna</p></th>
<th><p>Valor</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>HideTheRibbon</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>&lt;CustomUI xmlns =&quot;https://schemas.microsoft.com/office/2006/01/CustomUI&quot; &gt; &lt;startFromScratch da faixa de opções =&quot;true&quot;/&gt;&lt;/CustomUI&gt;</p></td>
</tr>
</tbody>
</table>


## <a name="applying-a-custom-ribbon-when-access-starts"></a>Aplicando uma faixa de opções personalizada quando o Access é iniciado
=======
<br/>

A tabela a seguir lista as configurações de personalização da faixa de opções a serem armazenadas na tabela **USysRibbons**.

|Nome da coluna|Valor|
|:----------|:----|
|**RibbonName**|HideTheRibbon|
|**RibbonXML**|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a>Aplicar uma faixa de opções personalizada ao iniciar o Access
>>>>>>> mestre

Para aplicar uma faixa de opções personalizada de forma que ela esteja disponível quando o aplicativo for iniciado, use o seguinte procedimento:

1.  Siga o processo descrito anteriormente para disponibilizar a faixa de opções personalizada para o aplicativo.

2.  Feche e então reinicie o aplicativo.

<<<<<<< Cabeça
3.  Clique no **Botão do Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") e clique em **Opções do Access**.

4.  Clique na opção **Banco de Dados Atual** e, em seguida, na seção **Opções da Faixa de Opções e da Barra de Ferramentas**, clique na lista **Nome da Faixa de Opções** e selecione **HideTheRibbon**.
=======
3.  Escolha o **Botão do Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102")e escolha **Opções do Access**.

4.  Escolha a opção de **Banco de dados atual** e em seguida, na seção **Opções de barra de ferramentas e faixa de opções** , escolha a lista **Nome da faixa de opções** e selecione **HideTheRibbon**.
>>>>>>> mestre

5.  Feche e então reinicie o aplicativo.

> [!NOTE]
> [!OBSERVAçãO] Para saber mais sobre a interface do usuário da faixa de opções em outros aplicativos do Office, consulte [Visão geral da faixa de opções do Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


