---
title: Habilitar a mesclagem personalizada de formulários do InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: O recurso Mesclar Formulários do Microsoft InfoPath editor foi projetado para combinar os dados de vários formulários em um único formulário.
ms.openlocfilehash: e0e6bfc074829f262d7eef3cf7bf6a86c3b2253b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765597"
---
# <a name="enable-custom-merging-of-infopath-forms"></a>Habilitar a mesclagem personalizada de formulários do InfoPath

O recurso **Mesclar Formulários** do Microsoft InfoPath editor foi projetado para combinar os dados de vários formulários em um único formulário. Isso também é conhecida como agregação de dados. Se a mesclagem de formulários estiver habilitado, você pode clique na guia **arquivo** , clique em **Salvar &amp; enviar**, clique em **Mesclar Formulários** em **importação &amp; Link**e clique no botão de **Mesclar Formulários** para selecionar um ou mais formulários para mesclar com o formulário atualmente aberto. O formulário atualmente aberto é o destino e os formulários selecionados na caixa de diálogo **Mesclar Formulários** são conhecidos como formulários de origem.
  
A agregação de dados que é resultado da mesclagem de formulários pode incluir todos os dados que estão contidos em formulários de origem e destino ou somente uma parte dos dados originais. As operações padrão são as seguintes.
  
- Para elementos de repetição, os dados são inseridos em um local correspondente no documento de destino. Isso acontece quando o atributo **MaxOccurs** do elemento de destino for maior que 1. 
    
- Para não se repetem elementos (ou seja, para elementos onde **MaxOccurs** é "1"), os atributos dos elementos de origem são adicionados aos atributos do elemento de destino existentes. 
    
## <a name="creating-a-custom-transform"></a>Criando uma transformação personalizada

A operação padrão ao mesclar formulários funciona bem para formulários baseados no mesmo esquema XML. Em algumas circunstâncias, no entanto, você talvez prefira mesclar formulários baseados em diferentes esquemas ou substituir a operação de mesclagem padrão para formulários que são baseados no mesmo esquema. Para esses cenários, é possível criar uma transformação XSLT (XSL), que contém instruções de agregação de lista segura para a operação de mala direta. A transformação é aplicada ao tempo de mala direta para criar um documento DOM que contém as informações a serem importados, junto com as anotações especificando como incorporar essas informações no documento de destino. Essas anotações são atributos XML no namespace `http://schemas.microsoft.com/office/InfoPath/2003/aggregation`.
  
Os atributos XML e seus valores servem como instruções de agregação de lista segura sobre como cada nó é mesclado com o documento XML de destino. Esses atributos são descritos nas seções a seguir.
  
### <a name="select"></a>select

O atributo **agg:select** contém uma expressão XPath de absoluta que identifica o elemento de destino. 
  
### <a name="insert"></a>insert

Um valor de "insert" para o atributo **agg:action** instrui InfoPath para inserir o elemento de origem, como um filho do elemento de destino é especificado usando o atributo **agg:select** . Os filhos do elemento de origem estão incluídos na operação de inserção. O atributo **selectChild** permite selecionar um determinado local para a operação de inserção do nó. O atributo **order** é usado para especificar se os elementos de origem são inseridos existente antes de elementos de destino ou depois. O valor padrão se o atributo **order** não estiver presente é "após". 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a>replace

Um valor de "substituição" para o atributo **agg:action** instrui InfoPath para substituir cada um dos elementos destino conhecidos pelo atributo **Selecione** com o elemento de origem. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a>mergeAttributes

Se o valor do atributo **agg:action** for "mergeAttributes", os atributos do elemento de origem são mesclados com os atributos de cada um dos elementos destino referenciados pela **Selecionar** atributo. 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a>delete

Se o valor do atributo **agg:action** for "excluir", cada um dos elementos destino referenciados pela **Selecionar** atributo são excluídas do documento de destino. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

Em conjunto com os atributos especificados no `http://schemas.microsoft.com/office/InfoPath/2003/aggregation` namespace, use o `http://schemas.microsoft.com/office/infopath/2003/aggregation-target` namespace para indicar um objeto XSL que implementa a interface **IXMLDOMDocument**. Um dos membros dessa interface mais útil é o método **get-documentElement**.
  
### <a name="get-documentelement"></a>Get-documentElement

O **destino: get-documentElement** função fornece acesso ao modelo de objeto de documento do documento de destino. Ele pode ser usado para alterar a maneira como funciona a operação de mala direta com base no conteúdo atual do documento de destino. 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a>Etapas para a criação de uma mesclagem personalizada

1. Selecione os tipos de documentos de origem XML do qual você deseja mesclar os dados. Colete um exemplo representativo de cada tipo de documento de origem.
    
2. Derive o esquema XML de cada tipo de documento de origem XML para um formulário do InfoPath existente. Esta etapa é realizada facilmente exportando o esquema XML com o comando **Exportar arquivos de origem** , na guia **Publicar** do Backstage. Para documentos XML que não foram criados no InfoPath, você pode usar uma ferramenta como o Microsoft Visual Studio para criar um esquema de documento XML de exemplo, ou você pode criar um formulário de amostra do documento XML no InfoPath e clique em seguida exportar o esquema que InfoPath deriva t ele estrutura do documento. 
    
3. Identifica os dados que você deseja mesclar a partir de cada tipo de documento de origem XML. Esta etapa dependerá praticamente os requisitos das formas de origem e de destino. Para algumas formulários, convém copiar todos os dados do formulário de origem. Para outras pessoas, você talvez prefira apenas um ou dois elementos de documento XML de base do formulário. Ao identificar quais dados que você deseja mesclar, preste atenção extra para documentos de origem e de destino para garantir que os elementos mapeiam logicamente entre as duas formas.
    
4. Crie uma transformação em XSL para cada tipo de documento de origem XML. Ao configurar a mesclagem das seus formulários, esta etapa será levar mais tempo. A finalidade da transformação em XSL é transformar o documento XML fonte em um formato que pode ser mesclado com o formulário de destino. Ao projetar sua transform, decida se deseja usar de caminhos de local de XML, quanto a mesclagem de instruções de agregação de lista segura do InfoPath.
    
    Visual Studio é uma ferramenta conveniente para criar transformações XSL. Visual Studio fornece a cor de sintaxe e uma estrutura de tópicos do documento. Ele também fornece automaticamente marcas de fechamento para elementos de XSL, que podem ajudar a diminuir redundantes digitando e erros de ortografia para encontrar. Você também pode criar transformações XSL com um editor de texto como o bloco de notas.
    
    Comece com a transformação de identidade, que é simplesmente uma transformação em XSL que produz o mesmo arquivo XML que é de entrada:
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" 
        xmlns:agg="http://schemas.microsoft.com/office/infopath/2003/aggregation" 
        xmlns:target="http://schemas.microsoft.com/office/infopath/2003/aggregation-target" 
        xmlns:my="http://schemas.microsoft.com/office/infopath/2003/myXSD/2003-05-29T20:30:47"> 
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

    Em seguida, adicione as seções de modelo de substituição para os elementos que você deseja adicionar a ação especial para. Por exemplo, esse modelo altera um `<src:Task>` elemento em uma `<my:field1>` elemento e define o valor do **agg:action** atributo para "substituir". 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. Adicione os arquivos de transformação XSL e arquivos de esquema no modelo de formulário. Após derivados esquemas para cada tipo de documento de origem e criado uma transformação em XSL para converter cada tipo de documento, de forma que o InfoPath pode mesclar seus dados, adicioná-los ao como recursos ao seu formulário. Clique em **Arquivos de recursos** , na guia **dados** e clique em **Adicionar** na caixa de diálogo **Arquivos de recurso** , navegue até seu esquema ou o arquivo de transformação XSL e, em seguida, clique em **Okey**. Faça isso para cada arquivo de esquema e o arquivo de transformação XSL que você criou.
    
    Se os esquemas que você adicionar usam o atributo **targetNamespace** , você deve adicionar um elemento de propriedade para o arquivo. xsf do formulário para que o namespace do esquema de reconheça do InfoPath. Para acessar esse arquivo, clique na guia **arquivo** , clique em **Publicar**e, em seguida, clique em **Exportar arquivos de origem**. Selecione um local para os arquivos e clique em **Okey**. Feche o modelo de formulário do InfoPath que você está criando.
    
    Navegue até o local que você especificou para os arquivos extraídos e localize o arquivo que tenha uma extensão de nome de arquivo. xsf. Geralmente, esse arquivo é chamado xsf. Encontre de abrir o arquivo no bloco de notas, o `<xsf:file>` marca que corresponde ao seu esquema e adicionar um elemento de propriedade de "namespace" para especificar o **targetNamespace** , conforme mostrado no exemplo a seguir. 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. A última etapa da preparação do seu formulário para dar suporte a mesclagem personalizada é atualizar o elemento **importParameters** no arquivo. xsf associado ao formulário. 

    Primeiro, encontre o `<xsf:importParameters>` marca no arquivo. xsf. Para cada par de transformação de esquema/XSL você criou para o seu formulário, adicione um elemento **xsf: importSource** ao elemento **xsf:importParameters** : `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`. 
    
    O atributo **name** do elemento **xsf: importSource** contém o nome do modelo de formulário que pode ser encontrado em um documento XML de origem. Geralmente, você pode deixar esta vazio. O atributo do **esquema** contém o nome de um arquivo de esquema adicionados ao modelo de formulário na etapa anterior. Finalmente, o atributo **transform** contém o nome da transformação em XSL que você deseja usar para converter os formulários que estão em conformidade com o esquema. 
    
    Você pode usar uma transformação personalizada com o evento [Mesclar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) ou por conta própria. 
    
## <a name="creating-a-custom-merge-in-code"></a>Criando uma mesclagem personalizada no código

Sinalizador mesclar com código é suportado usando o manipulador de eventos [Mesclar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) com seu atributo **useScriptHandler** correspondente do elemento **importParameters** no arquivo. xsf associado ao formulário. 

Em código gerenciado, você pode habilitar o evento [Mesclar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) marcando a caixa **Mesclar usando código personalizado**, e clicando no botão **Editar** , na categoria **Avançado** da caixa de diálogo **Opções de formulário** disponível no Backstage. 
  

