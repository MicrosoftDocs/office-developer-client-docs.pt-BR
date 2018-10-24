---
title: Habilitar a mesclagem personalizada de formulários do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: O recurso Mesclar Formulários do editor do Microsoft InfoPath foi projetado para combinar dados de vários formulários em um único formulário.
ms.openlocfilehash: 598c44bfe63a31237bf82ceb2212b001fbe7cc1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386912"
---
# <a name="enable-custom-merging-of-infopath-forms"></a>Habilitar a mesclagem personalizada de formulários do InfoPath

O recurso **Mesclar Formulários** do editor do Microsoft InfoPath foi projetado para combinar dados de vários formulários em um único formulário, o que também é conhecido como agregação de dados. Se a mesclagem de formulários estiver habilitada, você pode clicar na guia **Arquivo**, em **Salvar e Enviar**, em **Mesclar Formulários** sob **Importar e Vincular** e, em seguida, clicar no botão **Mesclar Formulários** para selecionar um ou mais formulários a mesclar com o formulário aberto no momento. O formulário aberto no momento é o formulário de destino e os formulários selecionados na caixa de diálogo **Mesclar Formulários** são chamados de formulários de origem.
  
A agregação de dados resultante da mesclagem de formulários pode incluir todos os dados contidos nos formulários de origem e de destino ou apenas uma parte dos dados originais. As operações padrão estão a seguir.
  
- Para elementos que se repetem, os dados são inseridos em um local correspondente no documento de destino. Isso ocorre quando o atributo **MaxOccurs** do elemento de destino for maior que 1. 
    
- Para elementos que não se repetem (ou seja, elementos em que **MaxOccurs** é "1"), os atributos dos elementos de origem são adicionados aos atributos existentes do elemento de destino. 
    
## <a name="creating-a-custom-transform"></a>Criar um cabeçalho personalizado

A operação padrão ao mesclar formulários funciona bem em formulários com base no mesmo esquema XML. Entretanto, em algumas circunstâncias, talvez você queira mesclar formulários com base em diferentes esquemas, ou substituir a operação de mesclagem padrão para formulários que tenham o mesmo esquema como base. Nesses cenários, você pode criar uma Transformação XSL (XSLT), que contém instruções de agregação para a operação de mesclagem. A transformação é aplicada no momento da mesclagem para criar um documento DOM que contém as informações a importar, juntamente das anotações que especificam como incorporar essas informações no documento de destino. Essas anotações são os atributos XML no namespace `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`.
  
Os atributos XML e seus valores servem como instruções de agregação sobre como cada nó é mesclado com o documento XML de destino. Esses atributos são descritos nas seções a seguir.
  
### <a name="select"></a>select

O atributo **agg:select** contém uma expressão XPath absoluta que identifica o elemento de destino. 
  
### <a name="insert"></a>insert

O valor de "insert" para o atributo **agg:action** instrui o InfoPath a inserir o elemento de origem como filho do elemento de destino especificado usando o atributo **agg:select**. Os filhos do elemento de origem são incluídos na operação de inserção. O atributo **selectChild** permite que você selecione um determinado local para a operação do nó de inserção. O atributo **order** é usado para especificar se os elementos de origem são inseridos antes ou depois dos elementos de destino existentes. O valor padrão é "depois" se o atributo **order** não estiver presente. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a>replace

O valor de "replace" para o atributo **agg:action** instrui o InfoPath a substituir cada um dos elementos de destino citados pelo atributo **select** pelo elemento de origem. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a>mergeAttributes

Se o valor do atributo **agg:action** for "mergeAttributes", os atributos do elemento de origem são mesclados aos atributos de cada um dos elementos de destino citados pelo atributo **select**. 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a>delete

Se o valor do atributo **agg:action** for "delete", todos os elementos de destino citados pelo atributo **select** serão excluídos do documento de destino. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

Junto aos atributos especificados no namespace `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`, use o namespace `https://schemas.microsoft.com/office/infopath/2003/aggregation-target` para indicar um objeto XSL que implementa a interface **IXMLDOMDocument**. Um dos membros mais úteis dessa interface é o método **get-documentElement**.
  
### <a name="get-documentelement"></a>get-documentElement

A função **target:get-documentElement** fornece acesso ao Modelo de Objeto do Documento de destino. Ela pode ser usada para alterar a maneira como a operação de mesclagem funciona com base no conteúdo atual do documento de destino. 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a>Etapas para criar uma mesclagem personalizada

1. Selecione os tipos de documentos XML de origem dos quais você deseja mesclar os dados. Colete uma amostra representativa de cada tipo de documento de origem.
    
2. Obtenha o esquema XML para cada tipo de documento XML de origem para um formulário existente do InfoPath. Esta etapa é realizada com facilidade exportando o esquema XML com o comando **Exportar Arquivos de Origem** na guia **Publicar** do modo de exibição Backstage. Para documentos XML que não foram criados no InfoPath, você pode usar uma ferramenta como o Microsoft Visual Studio para criar um esquema do documento XML de exemplo, ou pode criar um formulário de exemplo a partir de um documento XML do InfoPath e exportar o esquema que o InfoPath obtém a partir da estrutura do documento. 
    
3. Identifique os dados que você deseja mesclar em cada tipo de documento XML de origem. Esta etapa depende quase completamente dos requisitos dos formulários de origem e de destino. Em alguns formulários, convém copiar todos os dados do formulário de origem. Em outros, talvez você queira apenas um ou dois elementos do documento XML subjacente do formulário. Ao identificar quais são os dados que você deseja mesclar, preste atenção aos documentos de origem e de destino para garantir que os elementos mapeiem logicamente os dois formulários.
    
4. Crie uma transformação XSL para cada tipo de documento XML de origem. Ao configurar a mesclagem de formulários, será esta etapa que levará mais tempo. O propósito da transformação XSL é transformar o documento XML de origem em um formato que possa ser mesclado com o formulário de destino. Ao criar a transformação, decida se quer usar a mesclagem de caminhos de locais de XML ou mesclar a partir das instruções de agregação do InfoPath.
    
    O Visual Studio é uma ferramenta conveniente para criar transformações XSL. O Visual Studio fornece uma estrutura de tópicos do documento e cores de sintaxe. Também fornece automaticamente o fechamento de marcas para elementos XSL, o que pode ajudar a diminuir a digitação redundante e erros de ortografia difíceis de encontrar. Você também pode criar transformações XSL com um editor de texto, como o Bloco de Notas.
    
    Comece com a transformação da identidade, que é simplesmente uma transformação XSL que gera o mesmo arquivo XML de entrada:
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="https://www.w3.org/1999/XSL/Transform" 
        xmlns:agg="https://schemas.microsoft.com/office/infopath/2003/aggregation" 
        xmlns:target="https://schemas.microsoft.com/office/infopath/2003/aggregation-target" 
        xmlns:my="https://schemas.microsoft.com/office/infopath/2003/myXSD/2003-05-29T20:30:47"> 
            <xsl:template match="/"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
            <xsl:template match="@* | node()"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
        </xsl:stylesheet>
    ```

    Depois adicione seções de substituição do modelo para os elementos aos quais você deseja adicionar um tratamento especial. Por exemplo, este modelo altera o elemento `<src:Task>` no elemento `<my:field1>` e define o valor do atributo **agg:action** como "replace". 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. Adicione arquivos de transformação XSL e de esquema ao modelo de formulário. Depois de obter os esquemas para cada tipo de documento de origem e criar uma transformação XSL para converter cada tipo de documento para que o InfoPath possa mesclar os dados, adicione-os como recursos ao seu formulário. Clique em **Arquivos de Recurso** na guia **Dados** e, em seguida, clique em **Adicionar** na caixa de diálogo **Arquivos de Recurso**, navegue até o arquivo de esquema ou transformação XSL e clique em **OK**. Faça isso para cada arquivo de esquema e de transformação XSL que você criou.
    
    Se os esquemas que você adicionou usam o atributo **targetNamespace**, é necessário adicionar um elemento de propriedade ao arquivo .xsf do formulário para que o InfoPath saiba o namespace do esquema. Para acessar esse arquivo, clique na guia **Arquivo**, em **Publicar** e em **Exportar Arquivos de Origem**. Selecione o local dos arquivos e clique em **OK**. Feche o modelo de formulário do InfoPath que você está desenvolvendo.
    
    Navegue até o local especificado para os arquivos extraídos e localize o arquivo com extensão de nome .xsf. Normalmente, esse arquivo chama-se manifest.xsf. Abra o arquivo no Bloco de Notas, encontre a marca `<xsf:file>` que corresponde ao seu esquema e adicione um elemento de propriedade "namespace" para especificar o **targetNamespace** como mostrado no exemplo a seguir. 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. A última etapa ao preparar seu formulário para oferecer suporte à mesclagem personalizada é atualizar o elemento **importParameters** no arquivo .xsf associado ao formulário. 

    Primeiro, localize a marca `<xsf:importParameters>` no arquivo .xsf. Para cada par de esquema/transformação XSL que você criou para seu formulário, adicione um elemento **xsf:importSource** ao elemento **xsf:importParameters**: `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`. 
    
    O atributo **name** do elemento **xsf:importSource** contém o nome do modelo de formulário que pode ser encontrado em um documento XML de origem. Normalmente, você pode deixá-lo em branco. O atributo **schema** contém o nome de um arquivo de esquema adicionado ao modelo de formulário na etapa anterior. Por fim, o atributo **transform** contém o nome da transformação XSL que você deseja usar para converter os formulários que estão de acordo com o esquema. 
    
    Você pode usar uma transformação personalizada com o evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) ou por conta própria. 
    
## <a name="creating-a-custom-merge-in-code"></a>Criar uma mesclagem personalizada com código

A mesclagem personalizada com código é compatível com o uso do manipulador de eventos [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx), com seu atributo **useScriptHandler** correspondente do elemento **importParameters** no arquivo .xsf associado ao formulário. 

No código gerenciado, você pode habilitar o evento [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) marcando a caixa **Mesclar usando código personalizado** e, em seguida, clicando no botão **Editar**, na categoria **Avançado** da caixa de diálogo **Opções de Formulário** disponível no modo de exibição Backstage. 
  

