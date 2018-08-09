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
# <a name="enable-custom-merging-of-infopath-forms"></a><span data-ttu-id="b4525-103">Habilitar a mesclagem personalizada de formulários do InfoPath</span><span class="sxs-lookup"><span data-stu-id="b4525-103">Enable Custom Merging of InfoPath Forms</span></span>

<span data-ttu-id="b4525-104">O recurso **Mesclar Formulários** do Microsoft InfoPath editor foi projetado para combinar os dados de vários formulários em um único formulário.</span><span class="sxs-lookup"><span data-stu-id="b4525-104">The **Merge Forms** feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form.</span></span> <span data-ttu-id="b4525-105">Isso também é conhecida como agregação de dados.</span><span class="sxs-lookup"><span data-stu-id="b4525-105">This is also known as data aggregation.</span></span> <span data-ttu-id="b4525-106">Se a mesclagem de formulários estiver habilitado, você pode clique na guia **arquivo** , clique em **Salvar &amp; enviar**, clique em **Mesclar Formulários** em **importação &amp; Link**e clique no botão de **Mesclar Formulários** para selecionar um ou mais formulários para mesclar com o formulário atualmente aberto.</span><span class="sxs-lookup"><span data-stu-id="b4525-106">If merging forms is enabled, you can click the **File** tab, click **Save &amp; Send**, click **Merge Forms** under **Import &amp; Link**, and then click the **Merge Forms** button to select one or more forms to merge with the currently opened form.</span></span> <span data-ttu-id="b4525-107">O formulário atualmente aberto é o destino e os formulários selecionados na caixa de diálogo **Mesclar Formulários** são conhecidos como formulários de origem.</span><span class="sxs-lookup"><span data-stu-id="b4525-107">The form that is currently open is the target form and the forms selected in the **Merge Forms** dialog box are known as the source forms.</span></span>
  
<span data-ttu-id="b4525-108">A agregação de dados que é resultado da mesclagem de formulários pode incluir todos os dados que estão contidos em formulários de origem e destino ou somente uma parte dos dados originais.</span><span class="sxs-lookup"><span data-stu-id="b4525-108">The aggregation of data that results from merging forms can include all of the data that is contained in the source and target forms, or only a portion of the original data.</span></span> <span data-ttu-id="b4525-109">As operações padrão são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="b4525-109">The default operations are the following.</span></span>
  
- <span data-ttu-id="b4525-110">Para elementos de repetição, os dados são inseridos em um local correspondente no documento de destino.</span><span class="sxs-lookup"><span data-stu-id="b4525-110">For repeating elements, data is inserted at a matching location in the target document.</span></span> <span data-ttu-id="b4525-111">Isso acontece quando o atributo **MaxOccurs** do elemento de destino for maior que 1.</span><span class="sxs-lookup"><span data-stu-id="b4525-111">This happens when the **MaxOccurs** attribute of the destination element is greater than 1.</span></span> 
    
- <span data-ttu-id="b4525-112">Para não se repetem elementos (ou seja, para elementos onde **MaxOccurs** é "1"), os atributos dos elementos de origem são adicionados aos atributos do elemento de destino existentes.</span><span class="sxs-lookup"><span data-stu-id="b4525-112">For non-repeating elements (that is, for elements where **MaxOccurs** is "1"), the attributes of the source elements are added to the existing attributes of the destination element.</span></span> 
    
## <a name="creating-a-custom-transform"></a><span data-ttu-id="b4525-113">Criando uma transformação personalizada</span><span class="sxs-lookup"><span data-stu-id="b4525-113">Creating a Custom Transform</span></span>

<span data-ttu-id="b4525-114">A operação padrão ao mesclar formulários funciona bem para formulários baseados no mesmo esquema XML.</span><span class="sxs-lookup"><span data-stu-id="b4525-114">The default operation when merging forms works well for forms that are based on the same XML schema.</span></span> <span data-ttu-id="b4525-115">Em algumas circunstâncias, no entanto, você talvez prefira mesclar formulários baseados em diferentes esquemas ou substituir a operação de mesclagem padrão para formulários que são baseados no mesmo esquema.</span><span class="sxs-lookup"><span data-stu-id="b4525-115">In some circumstances, however, you may want to merge forms that are based on different schemas or override the default merge operation for forms that are based on the same schema.</span></span> <span data-ttu-id="b4525-116">Para esses cenários, é possível criar uma transformação XSLT (XSL), que contém instruções de agregação de lista segura para a operação de mala direta.</span><span class="sxs-lookup"><span data-stu-id="b4525-116">For these scenarios, you can create an XSL Transform (XSLT), which contains aggregation instructions for the merge operation.</span></span> <span data-ttu-id="b4525-117">A transformação é aplicada ao tempo de mala direta para criar um documento DOM que contém as informações a serem importados, junto com as anotações especificando como incorporar essas informações no documento de destino.</span><span class="sxs-lookup"><span data-stu-id="b4525-117">The transform is applied at merge time to create a DOM document that contains the information to be imported, together with annotations specifying how to incorporate this information into the target document.</span></span> <span data-ttu-id="b4525-118">Essas anotações são atributos XML no namespace `http://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span><span class="sxs-lookup"><span data-stu-id="b4525-118">These annotations are XML attributes in the namespace  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span></span>
  
<span data-ttu-id="b4525-119">Os atributos XML e seus valores servem como instruções de agregação de lista segura sobre como cada nó é mesclado com o documento XML de destino.</span><span class="sxs-lookup"><span data-stu-id="b4525-119">The XML attributes and their values serve as aggregation instructions on how each node is merged with the destination XML document.</span></span> <span data-ttu-id="b4525-120">Esses atributos são descritos nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="b4525-120">These attributes are described in the following sections.</span></span>
  
### <a name="select"></a><span data-ttu-id="b4525-121">select</span><span class="sxs-lookup"><span data-stu-id="b4525-121">select</span></span>

<span data-ttu-id="b4525-122">O atributo **agg:select** contém uma expressão XPath de absoluta que identifica o elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="b4525-122">The **agg:select** attribute contains an absolute XPath expression which identifies the destination element.</span></span> 
  
### <a name="insert"></a><span data-ttu-id="b4525-123">insert</span><span class="sxs-lookup"><span data-stu-id="b4525-123">insert</span></span>

<span data-ttu-id="b4525-124">Um valor de "insert" para o atributo **agg:action** instrui InfoPath para inserir o elemento de origem, como um filho do elemento de destino é especificado usando o atributo **agg:select** .</span><span class="sxs-lookup"><span data-stu-id="b4525-124">A value of "insert" for the **agg:action** attribute instructs InfoPath to insert the source element as a child of the destination element that is specified by using the **agg:select** attribute.</span></span> <span data-ttu-id="b4525-125">Os filhos do elemento de origem estão incluídos na operação de inserção.</span><span class="sxs-lookup"><span data-stu-id="b4525-125">The children of the source element are included in the insert operation.</span></span> <span data-ttu-id="b4525-126">O atributo **selectChild** permite selecionar um determinado local para a operação de inserção do nó.</span><span class="sxs-lookup"><span data-stu-id="b4525-126">The **selectChild** attribute lets you select a certain location for the insert node operation.</span></span> <span data-ttu-id="b4525-127">O atributo **order** é usado para especificar se os elementos de origem são inseridos existente antes de elementos de destino ou depois.</span><span class="sxs-lookup"><span data-stu-id="b4525-127">The **order** attribute is used to specify whether the source elements are inserted before existing destination elements or after.</span></span> <span data-ttu-id="b4525-128">O valor padrão se o atributo **order** não estiver presente é "após".</span><span class="sxs-lookup"><span data-stu-id="b4525-128">The default value if the **order** attribute is not present is "after".</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a><span data-ttu-id="b4525-129">replace</span><span class="sxs-lookup"><span data-stu-id="b4525-129">replace</span></span>

<span data-ttu-id="b4525-130">Um valor de "substituição" para o atributo **agg:action** instrui InfoPath para substituir cada um dos elementos destino conhecidos pelo atributo **Selecione** com o elemento de origem.</span><span class="sxs-lookup"><span data-stu-id="b4525-130">A value of "replace" for the **agg:action** attribute instructs InfoPath to replace each of the destination elements referred to by the **select** attribute with the source element.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a><span data-ttu-id="b4525-131">mergeAttributes</span><span class="sxs-lookup"><span data-stu-id="b4525-131">mergeAttributes</span></span>

<span data-ttu-id="b4525-132">Se o valor do atributo **agg:action** for "mergeAttributes", os atributos do elemento de origem são mesclados com os atributos de cada um dos elementos destino referenciados pela **Selecionar** atributo.</span><span class="sxs-lookup"><span data-stu-id="b4525-132">If the value of the **agg:action** attribute is "mergeAttributes", the attributes of the source element are merged with the attributes of each of the destination elements referred to by the **select** attribute.</span></span> 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a><span data-ttu-id="b4525-133">delete</span><span class="sxs-lookup"><span data-stu-id="b4525-133">delete</span></span>

<span data-ttu-id="b4525-134">Se o valor do atributo **agg:action** for "excluir", cada um dos elementos destino referenciados pela **Selecionar** atributo são excluídas do documento de destino.</span><span class="sxs-lookup"><span data-stu-id="b4525-134">If the value of the **agg:action** attribute is "delete", each of the destination elements referred to by the **select** attribute are deleted from the destination document.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

<span data-ttu-id="b4525-135">Em conjunto com os atributos especificados no `http://schemas.microsoft.com/office/InfoPath/2003/aggregation` namespace, use o `http://schemas.microsoft.com/office/infopath/2003/aggregation-target` namespace para indicar um objeto XSL que implementa a interface **IXMLDOMDocument**.</span><span class="sxs-lookup"><span data-stu-id="b4525-135">In conjunction with the attributes specified in the  `http://schemas.microsoft.com/office/InfoPath/2003/aggregation` namespace, you use the  `http://schemas.microsoft.com/office/infopath/2003/aggregation-target` namespace to denote an XSL object that implements the interface **IXMLDOMDocument**.</span></span> <span data-ttu-id="b4525-136">Um dos membros dessa interface mais útil é o método **get-documentElement**.</span><span class="sxs-lookup"><span data-stu-id="b4525-136">One of the most useful members of this interface is the method **get-documentElement**.</span></span>
  
### <a name="get-documentelement"></a><span data-ttu-id="b4525-137">Get-documentElement</span><span class="sxs-lookup"><span data-stu-id="b4525-137">get-documentElement</span></span>

<span data-ttu-id="b4525-138">O **destino: get-documentElement** função fornece acesso ao modelo de objeto de documento do documento de destino.</span><span class="sxs-lookup"><span data-stu-id="b4525-138">The **target:get-documentElement** function provides access to the Document Object Model of the destination document.</span></span> <span data-ttu-id="b4525-139">Ele pode ser usado para alterar a maneira como funciona a operação de mala direta com base no conteúdo atual do documento de destino.</span><span class="sxs-lookup"><span data-stu-id="b4525-139">It can be used to change the way the merge operation works based on the current contents of the destination document.</span></span> 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a><span data-ttu-id="b4525-140">Etapas para a criação de uma mesclagem personalizada</span><span class="sxs-lookup"><span data-stu-id="b4525-140">Steps for Creating a Custom Merge</span></span>

1. <span data-ttu-id="b4525-141">Selecione os tipos de documentos de origem XML do qual você deseja mesclar os dados.</span><span class="sxs-lookup"><span data-stu-id="b4525-141">Select the kinds of XML source documents from which you want to merge data.</span></span> <span data-ttu-id="b4525-142">Colete um exemplo representativo de cada tipo de documento de origem.</span><span class="sxs-lookup"><span data-stu-id="b4525-142">Collect a representative sample of each kind of source document.</span></span>
    
2. <span data-ttu-id="b4525-143">Derive o esquema XML de cada tipo de documento de origem XML para um formulário do InfoPath existente.</span><span class="sxs-lookup"><span data-stu-id="b4525-143">Derive the XML schema for each kind of XML source document for an existing InfoPath form.</span></span> <span data-ttu-id="b4525-144">Esta etapa é realizada facilmente exportando o esquema XML com o comando **Exportar arquivos de origem** , na guia **Publicar** do Backstage.</span><span class="sxs-lookup"><span data-stu-id="b4525-144">This step is easily accomplished by exporting the XML schema with the **Export Source Files** command on the **Publish** tab of the Backstage.</span></span> <span data-ttu-id="b4525-145">Para documentos XML que não foram criados no InfoPath, você pode usar uma ferramenta como o Microsoft Visual Studio para criar um esquema de documento XML de exemplo, ou você pode criar um formulário de amostra do documento XML no InfoPath e clique em seguida exportar o esquema que InfoPath deriva t ele estrutura do documento.</span><span class="sxs-lookup"><span data-stu-id="b4525-145">For XML documents that were not created in InfoPath, you can use a tool such as Microsoft Visual Studio to create a schema from the sample XML document, or you can create a sample form from the XML document in InfoPath, and then export the schema that InfoPath derives from the document structure.</span></span> 
    
3. <span data-ttu-id="b4525-146">Identifica os dados que você deseja mesclar a partir de cada tipo de documento de origem XML.</span><span class="sxs-lookup"><span data-stu-id="b4525-146">Identify the data that you want to merge from each kind of XML source document.</span></span> <span data-ttu-id="b4525-147">Esta etapa dependerá praticamente os requisitos das formas de origem e de destino.</span><span class="sxs-lookup"><span data-stu-id="b4525-147">This step will depend almost entirely on the requirements of both your source and destination forms.</span></span> <span data-ttu-id="b4525-148">Para algumas formulários, convém copiar todos os dados do formulário de origem.</span><span class="sxs-lookup"><span data-stu-id="b4525-148">For some forms, you may want to copy all of the data from the source form.</span></span> <span data-ttu-id="b4525-149">Para outras pessoas, você talvez prefira apenas um ou dois elementos de documento XML de base do formulário.</span><span class="sxs-lookup"><span data-stu-id="b4525-149">For others, you may want only one or two elements from the form's underlying XML document.</span></span> <span data-ttu-id="b4525-150">Ao identificar quais dados que você deseja mesclar, preste atenção extra para documentos de origem e de destino para garantir que os elementos mapeiam logicamente entre as duas formas.</span><span class="sxs-lookup"><span data-stu-id="b4525-150">When identifying what data that you want to merge, pay extra attention to both the source and destination documents to ensure that the elements map logically between the two forms.</span></span>
    
4. <span data-ttu-id="b4525-151">Crie uma transformação em XSL para cada tipo de documento de origem XML.</span><span class="sxs-lookup"><span data-stu-id="b4525-151">Create an XSL transform for each kind of XML source document.</span></span> <span data-ttu-id="b4525-152">Ao configurar a mesclagem das seus formulários, esta etapa será levar mais tempo.</span><span class="sxs-lookup"><span data-stu-id="b4525-152">When configuring the merging of your forms, this step will take the most time.</span></span> <span data-ttu-id="b4525-153">A finalidade da transformação em XSL é transformar o documento XML fonte em um formato que pode ser mesclado com o formulário de destino.</span><span class="sxs-lookup"><span data-stu-id="b4525-153">The purpose of the XSL transform is to transform the source XML document into a format that can be merged with the destination form.</span></span> <span data-ttu-id="b4525-154">Ao projetar sua transform, decida se deseja usar de caminhos de local de XML, quanto a mesclagem de instruções de agregação de lista segura do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="b4525-154">When designing your transform, decide whether you want to use merging from XML location paths, or merging from InfoPath aggregation instructions.</span></span>
    
    <span data-ttu-id="b4525-155">Visual Studio é uma ferramenta conveniente para criar transformações XSL.</span><span class="sxs-lookup"><span data-stu-id="b4525-155">Visual Studio is a convenient tool for creating XSL transforms.</span></span> <span data-ttu-id="b4525-156">Visual Studio fornece a cor de sintaxe e uma estrutura de tópicos do documento.</span><span class="sxs-lookup"><span data-stu-id="b4525-156">Visual Studio provides syntax coloring and a document outline.</span></span> <span data-ttu-id="b4525-157">Ele também fornece automaticamente marcas de fechamento para elementos de XSL, que podem ajudar a diminuir redundantes digitando e erros de ortografia para encontrar.</span><span class="sxs-lookup"><span data-stu-id="b4525-157">It also automatically provides closing tags for your XSL elements, which can help decrease redundant typing and hard-to-find spelling errors.</span></span> <span data-ttu-id="b4525-158">Você também pode criar transformações XSL com um editor de texto como o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="b4525-158">You can also create XSL transforms with a text editor such as Notepad.</span></span>
    
    <span data-ttu-id="b4525-159">Comece com a transformação de identidade, que é simplesmente uma transformação em XSL que produz o mesmo arquivo XML que é de entrada:</span><span class="sxs-lookup"><span data-stu-id="b4525-159">Start with the identity transform, which is simply an XSL transform that outputs the same XML file that is input:</span></span>
    
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

    <span data-ttu-id="b4525-160">Em seguida, adicione as seções de modelo de substituição para os elementos que você deseja adicionar a ação especial para.</span><span class="sxs-lookup"><span data-stu-id="b4525-160">Then add overriding template sections for the elements you want to add special handling for.</span></span> <span data-ttu-id="b4525-161">Por exemplo, esse modelo altera um `<src:Task>` elemento em uma `<my:field1>` elemento e define o valor do **agg:action** atributo para "substituir".</span><span class="sxs-lookup"><span data-stu-id="b4525-161">For example, this template changes a  `<src:Task>` element into a  `<my:field1>` element and sets the value of the **agg:action** attribute to "replace".</span></span> 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. <span data-ttu-id="b4525-162">Adicione os arquivos de transformação XSL e arquivos de esquema no modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="b4525-162">Add the XSL transform files and schema files in the form template.</span></span> <span data-ttu-id="b4525-163">Após derivados esquemas para cada tipo de documento de origem e criado uma transformação em XSL para converter cada tipo de documento, de forma que o InfoPath pode mesclar seus dados, adicioná-los ao como recursos ao seu formulário.</span><span class="sxs-lookup"><span data-stu-id="b4525-163">After you have derived schemas for each kind of source document and created an XSL transform to convert each document type so that InfoPath can merge its data, add them to as resources to your form.</span></span> <span data-ttu-id="b4525-164">Clique em **Arquivos de recursos** , na guia **dados** e clique em **Adicionar** na caixa de diálogo **Arquivos de recurso** , navegue até seu esquema ou o arquivo de transformação XSL e, em seguida, clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="b4525-164">Click **Resource Files** on the **Data** tab, and then click **Add** in the **Resource Files** dialog box, browse to your schema or XSL transform file, and then click **OK**.</span></span> <span data-ttu-id="b4525-165">Faça isso para cada arquivo de esquema e o arquivo de transformação XSL que você criou.</span><span class="sxs-lookup"><span data-stu-id="b4525-165">Do this to for each schema file and XSL transform file that you created.</span></span>
    
    <span data-ttu-id="b4525-166">Se os esquemas que você adicionar usam o atributo **targetNamespace** , você deve adicionar um elemento de propriedade para o arquivo. xsf do formulário para que o namespace do esquema de reconheça do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="b4525-166">If the schemas that you add use the **targetNamespace** attribute, you must add a property element to the form's .xsf file so that InfoPath knows the namespace of the schema.</span></span> <span data-ttu-id="b4525-167">Para acessar esse arquivo, clique na guia **arquivo** , clique em **Publicar**e, em seguida, clique em **Exportar arquivos de origem**.</span><span class="sxs-lookup"><span data-stu-id="b4525-167">To access this file, click the **File** tab, click **Publish**, and then click **Export Source Files**.</span></span> <span data-ttu-id="b4525-168">Selecione um local para os arquivos e clique em **Okey**.</span><span class="sxs-lookup"><span data-stu-id="b4525-168">Select a location for the files, and then click **OK**.</span></span> <span data-ttu-id="b4525-169">Feche o modelo de formulário do InfoPath que você está criando.</span><span class="sxs-lookup"><span data-stu-id="b4525-169">Then close the InfoPath form template that you are designing.</span></span>
    
    <span data-ttu-id="b4525-170">Navegue até o local que você especificou para os arquivos extraídos e localize o arquivo que tenha uma extensão de nome de arquivo. xsf.</span><span class="sxs-lookup"><span data-stu-id="b4525-170">Browse to the location that you specified for the extracted files and find the file that has an .xsf file name extension.</span></span> <span data-ttu-id="b4525-171">Geralmente, esse arquivo é chamado xsf.</span><span class="sxs-lookup"><span data-stu-id="b4525-171">Usually, this file is called manifest.xsf.</span></span> <span data-ttu-id="b4525-172">Encontre de abrir o arquivo no bloco de notas, o `<xsf:file>` marca que corresponde ao seu esquema e adicionar um elemento de propriedade de "namespace" para especificar o **targetNamespace** , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="b4525-172">Open the file in Notepad, find the  `<xsf:file>` tag that corresponds to your schema, and add a "namespace" property element to specify the **targetNamespace** as shown in the following example.</span></span> 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. <span data-ttu-id="b4525-173">A última etapa da preparação do seu formulário para dar suporte a mesclagem personalizada é atualizar o elemento **importParameters** no arquivo. xsf associado ao formulário.</span><span class="sxs-lookup"><span data-stu-id="b4525-173">The last step in preparing your form to support custom merging is to update the **importParameters** element in the .xsf file associated with the form.</span></span> 

    <span data-ttu-id="b4525-174">Primeiro, encontre o `<xsf:importParameters>` marca no arquivo. xsf.</span><span class="sxs-lookup"><span data-stu-id="b4525-174">First, find the  `<xsf:importParameters>` tag in the .xsf file.</span></span> <span data-ttu-id="b4525-175">Para cada par de transformação de esquema/XSL você criou para o seu formulário, adicione um elemento **xsf: importSource** ao elemento **xsf:importParameters** : `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span><span class="sxs-lookup"><span data-stu-id="b4525-175">For each schema/XSL transform pair you have created for your form, add an **xsf:importSource** element to the **xsf:importParameters** element:  `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span></span> 
    
    <span data-ttu-id="b4525-176">O atributo **name** do elemento **xsf: importSource** contém o nome do modelo de formulário que pode ser encontrado em um documento XML de origem.</span><span class="sxs-lookup"><span data-stu-id="b4525-176">The **name** attribute of the **xsf:importSource** element contains the form template's name that may be found in a source XML document.</span></span> <span data-ttu-id="b4525-177">Geralmente, você pode deixar esta vazio.</span><span class="sxs-lookup"><span data-stu-id="b4525-177">Usually, you can leave this empty.</span></span> <span data-ttu-id="b4525-178">O atributo do **esquema** contém o nome de um arquivo de esquema adicionados ao modelo de formulário na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="b4525-178">The **schema** attribute contains the name of a schema file that you added to the form template in the previous step.</span></span> <span data-ttu-id="b4525-179">Finalmente, o atributo **transform** contém o nome da transformação em XSL que você deseja usar para converter os formulários que estão em conformidade com o esquema.</span><span class="sxs-lookup"><span data-stu-id="b4525-179">Finally, the **transform** attribute contains the name of the XSL transform that you want to use to convert forms that conform to the schema.</span></span> 
    
    <span data-ttu-id="b4525-180">Você pode usar uma transformação personalizada com o evento [Mesclar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) ou por conta própria.</span><span class="sxs-lookup"><span data-stu-id="b4525-180">You can use a custom transform either with the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event or on its own.</span></span> 
    
## <a name="creating-a-custom-merge-in-code"></a><span data-ttu-id="b4525-181">Criando uma mesclagem personalizada no código</span><span class="sxs-lookup"><span data-stu-id="b4525-181">Creating a Custom Merge in Code</span></span>

<span data-ttu-id="b4525-182">Sinalizador mesclar com código é suportado usando o manipulador de eventos [Mesclar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) com seu atributo **useScriptHandler** correspondente do elemento **importParameters** no arquivo. xsf associado ao formulário.</span><span class="sxs-lookup"><span data-stu-id="b4525-182">Custom merging with code is supported by using the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event handler, with its corresponding **useScriptHandler** attribute of the **importParameters** element in the .xsf file associated with the form.</span></span> 

<span data-ttu-id="b4525-183">Em código gerenciado, você pode habilitar o evento [Mesclar](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) marcando a caixa **Mesclar usando código personalizado**, e clicando no botão **Editar** , na categoria **Avançado** da caixa de diálogo **Opções de formulário** disponível no Backstage.</span><span class="sxs-lookup"><span data-stu-id="b4525-183">In managed code, you can enable the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event by checking the box **Merge using custom code**, and then clicking the **Edit** button, in the **Advanced** category of the **Form Options** dialog box available from the Backstage.</span></span> 
  

