---
title: Trabalhar com esquemas XML no InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c1d70e9f-b9fc-7bdb-107e-d0cd8191607b
description: Um modelo de formulário criado com o Microsoft InfoPath usa um esquema XML (XSD) para executar validação estrutural e de dados no XML que é entrada, edição e saída de um formulário do InfoPath. Cada modelo de formulário criado no designer de formulário do InfoPath contém pelo menos um arquivo de esquema XSD (.xsd) usado para validação em tempo de executar.
ms.openlocfilehash: 25828c3ec21d22a9952452d5a82fe1a3b4bab54c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303161"
---
# <a name="working-with-xml-schemas-in-infopath"></a><span data-ttu-id="259e0-104">Trabalhar com esquemas XML no InfoPath</span><span class="sxs-lookup"><span data-stu-id="259e0-104">Working with XML Schemas in InfoPath</span></span>

<span data-ttu-id="259e0-105">Um modelo de formulário criado com o Microsoft InfoPath usa um esquema XML (XSD) para executar validação estrutural e de dados no XML que é entrada, edição e saída de um formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="259e0-105">A form template that you create with Microsoft InfoPath uses an XML Schema (XSD) to perform structural and data validation on the XML that is input, edited, and output from an InfoPath form.</span></span> <span data-ttu-id="259e0-106">Cada modelo de formulário criado no designer de formulário do InfoPath contém pelo menos um arquivo de esquema XSD (.xsd) usado para validação em tempo de executar.</span><span class="sxs-lookup"><span data-stu-id="259e0-106">Every form template created in the InfoPath form designer contains at least one XSD schema file (.xsd) that is used for validation at run time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="259e0-107">As informações contidas neste tópico se aplica a modelos de formulário projetados para uso no editor do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="259e0-107">The information contained in this topic applies to form templates designed for use in the InfoPath editor.</span></span> <span data-ttu-id="259e0-108">Modelos de formulário compatíveis com navegador têm requisitos de esquema XSD mais rígidos.</span><span class="sxs-lookup"><span data-stu-id="259e0-108">Browser-compatible form templates have stricter XSD Schema requirements.</span></span> <span data-ttu-id="259e0-109">Para obter mais informações, consulte a documentação sobre esquemas XML em modelos de formulário compatíveis com navegador disponíveis no MSDN.</span><span class="sxs-lookup"><span data-stu-id="259e0-109">For more information, see the documentation about XML Schemas in browser-compatible form templates available on MSDN.</span></span> 
  
## <a name="using-externally-authored-xml-schemas"></a><span data-ttu-id="259e0-110">Usando esquemas XML de autoria externa</span><span class="sxs-lookup"><span data-stu-id="259e0-110">Using Externally-authored XML Schemas</span></span>

<span data-ttu-id="259e0-111">Para carregar um arquivo de esquema XSD que foi de autoria fora do InfoPath, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="259e0-111">To load an XSD schema file that was authored outside of InfoPath, follow these steps.</span></span>
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a><span data-ttu-id="259e0-112">Para criar um modelo de formulário com base em um esquema externo</span><span class="sxs-lookup"><span data-stu-id="259e0-112">To create a form template based on an external schema</span></span>

1. <span data-ttu-id="259e0-113">In the Backstage, click **New**, click **XML or Schema** under **Advanced Form Templates**, and then click **Design This Form**.</span><span class="sxs-lookup"><span data-stu-id="259e0-113">In the Backstage, click **New**, click **XML or Schema** under **Advanced Form Templates**, and then click **Design This Form**.</span></span>
    
2. <span data-ttu-id="259e0-114">No Assistente **de Fonte** de Dados, especifique o arquivo de esquema XSD que você deseja usar e clique em **Próximo** e conclua as páginas restantes do assistente.</span><span class="sxs-lookup"><span data-stu-id="259e0-114">In the **Data Source Wizard**, specify the XSD schema file you want to use, and then click **Next** and complete the remaining pages of the wizard.</span></span> 
    
## <a name="unsupported-xsd-constructs"></a><span data-ttu-id="259e0-115">Construções XSD sem suporte</span><span class="sxs-lookup"><span data-stu-id="259e0-115">Unsupported XSD Constructs</span></span>

<span data-ttu-id="259e0-116">As seções a seguir descrevem construções XSD que o InfoPath não pode manipular em tempo de executar.</span><span class="sxs-lookup"><span data-stu-id="259e0-116">The following sections describe XSD constructs that InfoPath cannot handle at run time.</span></span> <span data-ttu-id="259e0-117">Evite essas construções ao criar um modelo de formulário no designer de formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="259e0-117">Avoid these constructs when creating a form template in the InfoPath form designer.</span></span>
  
## <a name="entity-and-entities-types"></a><span data-ttu-id="259e0-118">Tipos de ENTIDADEs e ENTIDADEs</span><span class="sxs-lookup"><span data-stu-id="259e0-118">ENTITY and ENTITIES Types</span></span>

<span data-ttu-id="259e0-119">Os **tipos entity** e **ENTITIES** exigem uma DTD (definição de tipo de documento) para validação, que o InfoPath não dá suporte.</span><span class="sxs-lookup"><span data-stu-id="259e0-119">The **ENTITY** and **ENTITIES** types require a document type definition (DTD) for validation, which InfoPath does not support.</span></span> <span data-ttu-id="259e0-120">O InfoPath não permite que você projete um modelo de formulário em relação a esse esquema e exibe uma mensagem de erro que recomenda alterar o tipo **ENTITY** para o tipo **NCName** do qual ENTITY **deriva.**</span><span class="sxs-lookup"><span data-stu-id="259e0-120">InfoPath does not allow you to design a form template against such a schema and displays an error message that recommends changing the **ENTITY** type to the **NCName** type from which **ENTITY** derives.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="259e0-121">Se você criar manualmente um modelo de formulário do InfoPath fora do modo de design e ele usar um XSD que inclua tipos **entity** e **ENTITIES,** o modelo de formulário poderá funcionar em tempo de executar se o arquivo Template.xml contiver o DTD necessário para esses tipos.</span><span class="sxs-lookup"><span data-stu-id="259e0-121">If you manually author an InfoPath form template outside of design mode, and it uses an XSD that includes **ENTITY** and **ENTITIES** types, the form template may work at run time if the Template.xml file contains the required DTD for these types.</span></span> 
  
## <a name="required-xsdany-element"></a><span data-ttu-id="259e0-122">Elemento xsd:any necessário</span><span class="sxs-lookup"><span data-stu-id="259e0-122">Required xsd:any Element</span></span>

<span data-ttu-id="259e0-123">Uma ocorrência de um elemento **curinga xsd:any,** ou seja, uma ocorrência de um elemento **xsd:any** com um valor de atributo **minOccurs** maior que zero ("necessário qualquer"), impede que o InfoPath deterministicamente criar uma instância válida para esse fragmento de esquema.</span><span class="sxs-lookup"><span data-stu-id="259e0-123">An occurrence of an **xsd:any** wildcard element, that is, an occurrence of an **xsd:any** element with a **minOccurs** attribute value greater than zero ("required any"), prevents InfoPath from deterministically creating a valid instance for this schema fragment.</span></span> <span data-ttu-id="259e0-124">O InfoPath deve ser capaz de criar uma instância válida ao gerar um formulário que use esse fragmento de esquema.</span><span class="sxs-lookup"><span data-stu-id="259e0-124">InfoPath must be able to create a valid instance when generating a form that uses this schema fragment.</span></span> <span data-ttu-id="259e0-125">Como parte da execução do Assistente de Fonte de **Dados,** os esquemas com os elementos **xsd:any** necessários exigem que você escolha qual elemento de esquema deseja usar no lugar do elemento **xsd:any** necessário.</span><span class="sxs-lookup"><span data-stu-id="259e0-125">As part of running the **Data Source Wizard**, schemas with required **xsd:any** elements require you to choose which schema element you want to use in place of the required **xsd:any** element.</span></span> 
  
## <a name="elements-with-an-abstract-complex-type"></a><span data-ttu-id="259e0-126">Elementos com um tipo complexo abstrato</span><span class="sxs-lookup"><span data-stu-id="259e0-126">Elements with an Abstract Complex Type</span></span>

<span data-ttu-id="259e0-127">O modo de design do InfoPath dá suporte à criação de um modelo de formulário contra esquemas que usam tipos complexos abstratos.</span><span class="sxs-lookup"><span data-stu-id="259e0-127">InfoPath design mode supports designing a form template against schemas that use abstract complex types.</span></span> <span data-ttu-id="259e0-128">Por exemplo, se um elemento nomeado tem um tipo complexo abstrato chamado que tem duas derivações e  `shippingAddress`  `address` ,  `USAddress`  `CanadianAddress` InfoPath trata  `shippingAddress`  `shippingAddress`  `USAddress`  `shippingAddress` qualquer instância  `CanadianAddress` de como uma escolha entre com tipo e com tipo .</span><span class="sxs-lookup"><span data-stu-id="259e0-128">For example, if an element named  `shippingAddress` has an abstract complex type named  `address` that has two derivations,  `USAddress` and  `CanadianAddress`, InfoPath treats any instance of  `shippingAddress` as a choice between  `shippingAddress` with type  `USAddress` and  `shippingAddress` with type  `CanadianAddress` .</span></span> <span data-ttu-id="259e0-129">Neste exemplo, se os esquemas fornecidos não contêm tipos derivados do endereço, o InfoPath solicita um esquema adicional que atende a esse requisito.</span><span class="sxs-lookup"><span data-stu-id="259e0-129">In this example, if the provided schemas contain no types that derive from address, then InfoPath requests an additional schema that fulfills this requirement.</span></span> 
  
## <a name="xsd-constructs-with-reduced-functionality"></a><span data-ttu-id="259e0-130">Construções XSD com Funcionalidade Reduzida</span><span class="sxs-lookup"><span data-stu-id="259e0-130">XSD Constructs with Reduced Functionality</span></span>

<span data-ttu-id="259e0-131">As seções a seguir descrevem construções XSD que têm funcionalidade reduzida quando usadas para criar um modelo de formulário no designer de formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="259e0-131">The following sections describe XSD constructs that have reduced functionality when used to create a form template in the InfoPath form designer.</span></span>
  
## <a name="substitution-groups"></a><span data-ttu-id="259e0-132">Grupos de substituição</span><span class="sxs-lookup"><span data-stu-id="259e0-132">Substitution Groups</span></span>

<span data-ttu-id="259e0-133">Todos os membros do grupo de substituição aparecem no painel **de tarefas** Campos.</span><span class="sxs-lookup"><span data-stu-id="259e0-133">All members of the substitution group appear in the **Fields** task pane.</span></span> <span data-ttu-id="259e0-134">O InfoPath representa as possibilidades de substituição como uma escolha de todos os grupos de substituição (incluindo o elemento de definição, se não for abstrato).</span><span class="sxs-lookup"><span data-stu-id="259e0-134">InfoPath represents the substitution possibilities as a choice of all the substitution groups (including the defining element, if it is not abstract).</span></span> <span data-ttu-id="259e0-135">Se não houver grupos de substituição para um elemento abstrato, o InfoPath solicitará que você forneça um esquema que contenha pelo menos um elemento que seja um grupo de substituição.</span><span class="sxs-lookup"><span data-stu-id="259e0-135">If there are no substitution groups for an abstract element, InfoPath prompts you to provide a schema that contains at least one element that is a substitution group.</span></span> 
  
## <a name="unbounded-choice-elements"></a><span data-ttu-id="259e0-136">Elementos de escolha não acondido</span><span class="sxs-lookup"><span data-stu-id="259e0-136">Unbounded Choice Elements</span></span>

<span data-ttu-id="259e0-137">O fragmento de esquema a seguir mostra um elemento de escolha nãobounded:</span><span class="sxs-lookup"><span data-stu-id="259e0-137">The following schema fragment shows an unbounded choice element:</span></span>
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

<span data-ttu-id="259e0-138">O InfoPath exibe elementos de escolha repetidos como opções repetidas no painel **de** tarefas Campos.</span><span class="sxs-lookup"><span data-stu-id="259e0-138">InfoPath displays repeating choice elements as repeating choices in the **Fields** task pane.</span></span> <span data-ttu-id="259e0-139">Há um controle grupo de **escolha** de repetição que você pode usar para representar a lista heterogênea definida pelo elemento de opção de repetição no XSD.</span><span class="sxs-lookup"><span data-stu-id="259e0-139">There is a **Repeating Choice Group** control that you can use to represent the heterogeneous list defined by the repeating choice element in the XSD.</span></span> 
  
## <a name="repeating-sequence"></a><span data-ttu-id="259e0-140">Sequência de repetição</span><span class="sxs-lookup"><span data-stu-id="259e0-140">Repeating Sequence</span></span>

<span data-ttu-id="259e0-141">O fragmento de esquema a seguir mostra uma sequência de repetição:</span><span class="sxs-lookup"><span data-stu-id="259e0-141">The following schema fragment shows a repeating sequence:</span></span>
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

<span data-ttu-id="259e0-142">Desde que a sequência de repetição contenha um elemento necessário, o InfoPath carrega o XSD sem modificá-lo e permite vincular controles de seção repetitivas à sequência de repetição.</span><span class="sxs-lookup"><span data-stu-id="259e0-142">As long as the repeating sequence contains a required element, InfoPath loads the XSD without modifying it and allows you to bind repeating section controls to the repeating sequence.</span></span>
  
## <a name="choice-of-model-groups"></a><span data-ttu-id="259e0-143">Escolha de grupos de modelos</span><span class="sxs-lookup"><span data-stu-id="259e0-143">Choice of Model Groups</span></span>

<span data-ttu-id="259e0-144">O fragmento de esquema a seguir mostra o elemento de escolha que contém vários grupos de modelos:</span><span class="sxs-lookup"><span data-stu-id="259e0-144">The following schema fragment shows the choice element containing several model groups:</span></span>
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

<span data-ttu-id="259e0-145">O modo de design do InfoPath dá suporte a tais construções XSD sem a necessidade de qualquer modificação feita pelo designer de formulário.</span><span class="sxs-lookup"><span data-stu-id="259e0-145">InfoPath design mode supports such XSD constructs without requiring any modification by the form designer.</span></span> <span data-ttu-id="259e0-146">Embora o InfoPath não modifique o significado do esquema, ele simplifica o constructo de escolha acima em uma única opção recolhido equivalente no painel de tarefas Campos. </span><span class="sxs-lookup"><span data-stu-id="259e0-146">While InfoPath does not modify the meaning of the schema, it simplifies the choice construct above into an equivalent collapsed single choice in the **Fields** task pane.</span></span> 
  
## <a name="optional-sibling-with-same-qualified-name"></a><span data-ttu-id="259e0-147">Irmão opcional com o mesmo nome qualificado</span><span class="sxs-lookup"><span data-stu-id="259e0-147">Optional Sibling with Same Qualified Name</span></span>

<span data-ttu-id="259e0-148">O fragmento de esquema a seguir mostra um irmão opcional com o mesmo nome qualificado ( `QName` ):</span><span class="sxs-lookup"><span data-stu-id="259e0-148">The following schema fragment shows an optional sibling with same qualified name (`QName`):</span></span>
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

<span data-ttu-id="259e0-149">**Expressões XPath** para esses nós podem ser complexas porque cada instância XML potencial deve ser contabilada no designer de formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="259e0-149">**XPath** expressions for these nodes can be complex because every potential XML instance must be accounted for in the InfoPath form designer.</span></span> <span data-ttu-id="259e0-150">O InfoPath não expõe partes do esquema para o qual ele pode ter dificuldade para criar ligações **XPath** corretas.</span><span class="sxs-lookup"><span data-stu-id="259e0-150">InfoPath does not expose parts of the schema for which it may have difficulty creating correct **XPath** bindings.</span></span> <span data-ttu-id="259e0-151">Os avisos são exibidos em relação às partes do esquema que são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="259e0-151">Warnings appear regarding the portions of the schema that are ignored.</span></span> 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a><span data-ttu-id="259e0-152">Construções XSD com significado especial no InfoPath</span><span class="sxs-lookup"><span data-stu-id="259e0-152">XSD Constructs with Special Meaning in InfoPath</span></span>

<span data-ttu-id="259e0-153">As seções a seguir descrevem construções XSD que têm significado especial quando usadas na criação de um modelo de formulário no modo de design.</span><span class="sxs-lookup"><span data-stu-id="259e0-153">The following sections describe XSD constructs that have special meaning when used in creating a form template in design mode.</span></span> <span data-ttu-id="259e0-154">Estas seções descrevem como você pode usar as construções em seu esquema para habilitar determinados comportamentos.</span><span class="sxs-lookup"><span data-stu-id="259e0-154">These sections describe how you can use the constructs in your schema to enable certain behaviors.</span></span>
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a><span data-ttu-id="259e0-155">Adicionando novos campos e grupos de elementos com o painel de tarefas Fields</span><span class="sxs-lookup"><span data-stu-id="259e0-155">Adding New Element Fields and Groups with the Fields Task Pane</span></span>

<span data-ttu-id="259e0-156">Você pode construir seu esquema para que possa usar o painel de tarefas **Campos** para adicionar novos campos e grupos de elementos a um elemento em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="259e0-156">You can construct your schema so that you can use the **Fields** task pane to add new element fields and groups to an element at design time.</span></span> <span data-ttu-id="259e0-157">Para fazer isso, você declara um elemento em seu esquema com um elemento **xsd:any** opcional não-bounded que especifica o atributo de namespace com o caractere **curinga ##any.**</span><span class="sxs-lookup"><span data-stu-id="259e0-157">To do so, you declare an element in your schema with an optional, unbounded **xsd:any** element that specifies the namespace attribute with the **##any** wildcard.</span></span> <span data-ttu-id="259e0-158">Em seguida, no modo de design, você pode usar o painel de tarefas **Campos** para adicionar novos campos e grupos de elementos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="259e0-158">Then, in design mode, you can use the **Fields** task pane to add new element fields and groups to that element.</span></span> <span data-ttu-id="259e0-159">Por exemplo, você poderia adicionar novo conteúdo ao seguinte elemento:</span><span class="sxs-lookup"><span data-stu-id="259e0-159">For example, you could add new content to the following element:</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a><span data-ttu-id="259e0-160">Adicionando novos campos de atributo com o painel de tarefas Fields</span><span class="sxs-lookup"><span data-stu-id="259e0-160">Adding New Attribute Fields with the Fields Task Pane</span></span>

<span data-ttu-id="259e0-161">Da mesma forma que o caso do elemento, você pode declarar um atributo com um elemento **anyAttribute** que tenha o atributo namespace especificado como o caractere curinga **##any.**</span><span class="sxs-lookup"><span data-stu-id="259e0-161">Similarly to the element case, you can declare an attribute with an **anyAttribute** element that has the namespace attribute specified as the **##any** wildcard.</span></span> <span data-ttu-id="259e0-162">No tempo de design, você pode usar o painel de tarefas **Fields** para adicionar novo conteúdo a esse atributo de esquema.</span><span class="sxs-lookup"><span data-stu-id="259e0-162">At design time, you can use the **Fields** task pane to add new content to that schema attribute.</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a><span data-ttu-id="259e0-163">Armazenar assinaturas XML na fonte de dados</span><span class="sxs-lookup"><span data-stu-id="259e0-163">Storing XML Signatures in the Data Source</span></span>

<span data-ttu-id="259e0-164">Para permitir que os usuários assinem digitalmente um formulário em tempo de executar, o esquema da fonte de dados deve declarar um elemento nomeado assinatura para armazenar as informações de assinaturas XML (assinatura digital) criadas quando um usuário assina o formulário.</span><span class="sxs-lookup"><span data-stu-id="259e0-164">To enable users to digitally sign a form at run time, the schema of the data source must declare an element named signature for storing the XML Signatures (digital signature) information that is created when a user signs the form.</span></span> <span data-ttu-id="259e0-165">Faça essa declaração usando o elemento **xsd:any** com o atributo namespace especificado como o namespace de Assinaturas XML com um caractere curinga, da seguinte forma: https://www.w3c.org/2000/09/xmldsig# "</span><span class="sxs-lookup"><span data-stu-id="259e0-165">You make this declaration by using the **xsd:any** element with the namespace attribute specified as the XML Signatures namespace with a wildcard character, as follows: "https://www.w3c.org/2000/09/xmldsig#"</span></span> 
  
```XML
<xsd:element name="signature"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="https://www.w3c.org/2000/09/xmldsig#"  
             processContents="lax" minOccurs="0" maxOccurs="unbounded"/> 
        <xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="binding-a-field-to-a-rich-text-box-control"></a><span data-ttu-id="259e0-166">Binding a Field to a Rich Text Box Control</span><span class="sxs-lookup"><span data-stu-id="259e0-166">Binding a Field to a Rich Text Box Control</span></span>

 <span data-ttu-id="259e0-167">**Os controles Rich Text Box** no InfoPath geram XHTML genérico; consequentemente, seu esquema deve especificar que qualquer número de texto e nós XHTML é válido no XML da instância do formulário.</span><span class="sxs-lookup"><span data-stu-id="259e0-167">**Rich Text Box** controls in InfoPath generate generic XHTML; consequently, your schema must specify that any number of text and XHTML nodes is valid in the XML of the form instance.</span></span> <span data-ttu-id="259e0-168">Você pode obter essa especificação com o seguinte constructo XSD:</span><span class="sxs-lookup"><span data-stu-id="259e0-168">You can achieve this specification with the following XSD construct:</span></span> 
  
```XML
<xsd:element name="xhtml"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="https://www.w3.org/1999/xhtml" processContents="lax"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

> [!NOTE]
> <span data-ttu-id="259e0-169">O InfoPath nunca modifica o conteúdo do arquivo de esquema (.xsd), mas pode inferir logicamente um subconjunto dele para fins de design.</span><span class="sxs-lookup"><span data-stu-id="259e0-169">InfoPath never modifies the content of the schema file (.xsd), but it may logically infer a subset of it for design purposes.</span></span> <span data-ttu-id="259e0-170">O arquivo de esquema é sempre intocado dentro do modelo de formulário no tempo de design e no tempo de executar.</span><span class="sxs-lookup"><span data-stu-id="259e0-170">The schema file is always untouched within the form template at both design time and run time.</span></span> 
  
## <a name="debugging-common-xsd-errors"></a><span data-ttu-id="259e0-171">Depurando erros comuns de XSD</span><span class="sxs-lookup"><span data-stu-id="259e0-171">Debugging Common XSD Errors</span></span>

<span data-ttu-id="259e0-172">Se você carregar arquivos XSD criado externamente para criar modelos de formulário no designer de formulário do InfoPath, poderá receber um dos dois tipos de mensagens de erro: mensagens de erro MSXML ou mensagens de erro do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="259e0-172">If you load externally authored XSD files to create form templates in the InfoPath form designer, you may receive either of two types of error messages: MSXML error messages or InfoPath error messages.</span></span> <span data-ttu-id="259e0-173">As mensagens de erro MSXML aparecem na seção Detalhes de uma caixa de diálogo de mensagem de erro do InfoPath e sempre começam com uma referência ao nome ou caminho do arquivo de esquema que está aparecendo o erro. </span><span class="sxs-lookup"><span data-stu-id="259e0-173">MSXML error messages appear in the **Details** section of an InfoPath error message dialog box, and they always begin with a reference to the name or path of the schema file that is raising the error.</span></span> <span data-ttu-id="259e0-174">Algumas construções válidas de esquema XSD não são suportadas pelo InfoPath; eles são discutidos na seção Unsupported XSD Constructs.</span><span class="sxs-lookup"><span data-stu-id="259e0-174">Some valid XSD schema constructs are not supported by InfoPath; these are discussed in the Unsupported XSD Constructs section.</span></span> <span data-ttu-id="259e0-175">As seções a seguir descrevem alguns erros comuns que podem fazer com que os esquemas não carreguem com êxito no InfoPath.</span><span class="sxs-lookup"><span data-stu-id="259e0-175">The following sections describe some common errors that can cause schemas to fail to load successfully in InfoPath.</span></span> 
  
## <a name="the-xsd-namespace-declaration"></a><span data-ttu-id="259e0-176">A declaração de namespace XSD</span><span class="sxs-lookup"><span data-stu-id="259e0-176">The XSD Namespace Declaration</span></span>

<span data-ttu-id="259e0-177">Semelhante a todos os padrões W3C, os esquemas XML (XSD) passaram por um processo de revisão demorado em sua maneira de se tornar uma recomendação.</span><span class="sxs-lookup"><span data-stu-id="259e0-177">Similar to all W3C standards, XML Schemas (XSD) went through a lengthy review process on its way to becoming a recommendation.</span></span> <span data-ttu-id="259e0-178">Havia muitos rascunhos de trabalho e, consequentemente, muitos arquivos XSD foram escritos com base nesses padrões em evolução.</span><span class="sxs-lookup"><span data-stu-id="259e0-178">There were many working drafts, and consequently, many XSD files were written based on these evolving standards.</span></span> <span data-ttu-id="259e0-179">Durante esse processo, a Microsoft criou uma linguagem de esquema proprietária chamada XML-Data Reduced (XDR) incluída no MSXML 3.0.</span><span class="sxs-lookup"><span data-stu-id="259e0-179">During this process, Microsoft created a proprietary schema language called XML-Data Reduced (XDR) that was included with MSXML 3.0.</span></span> <span data-ttu-id="259e0-180">A partir do lançamento do MSXML 4.0, o Microsoft XML Core Services dá suporte à recomendação completa do XSD.</span><span class="sxs-lookup"><span data-stu-id="259e0-180">Starting with the release of MSXML 4.0, Microsoft XML Core Services supports the full recommendation of XSD.</span></span> <span data-ttu-id="259e0-181">Muitos programas para a criação de esquemas não aguardaram até que o XSD se torne uma recomendação completa.</span><span class="sxs-lookup"><span data-stu-id="259e0-181">Many programs for creating schemas did not wait for XSD to become a full recommendation.</span></span> <span data-ttu-id="259e0-182">Versões mais antigas desses programas podem produzir arquivos XSD desatualizados aos quais a infraestrutura MSXML 5.0, da qual depende o InfoPath, não dá suporte.</span><span class="sxs-lookup"><span data-stu-id="259e0-182">Older versions of these programs may produce outdated XSD files that the MSXML 5.0 infrastructure, on which InfoPath depends, does not support.</span></span>
  
<span data-ttu-id="259e0-183">Para garantir que um arquivo XSD suporte a recomendação XSD completa, ele deve conter a seguinte declaração de namespace XML na marca \< de \> esquema:</span><span class="sxs-lookup"><span data-stu-id="259e0-183">To ensure that an XSD file supports the full XSD recommendation, it should contain the following XML namespace declaration in the \<schema\> tag:</span></span>
  
```XML
xmlns:xsd="https://www.w3.org/2001/XMLSchema"
```

<span data-ttu-id="259e0-184">Semelhante a todas as declarações de namespace XML, o prefixo XML (neste caso ' xsd') pode ser qualquer cadeia de caracteres de prefixo válida.</span><span class="sxs-lookup"><span data-stu-id="259e0-184">Similar to all XML namespace declarations, the XML prefix (in this case 'xsd') can be any valid prefix string.</span></span> <span data-ttu-id="259e0-185">Alguns prefixos comuns que você pode ver na prática são 'xsd', 'xs' e '' (sem prefixo).</span><span class="sxs-lookup"><span data-stu-id="259e0-185">Some common prefixes you may see in practice are 'xsd', 'xs', and '' (no prefix).</span></span> <span data-ttu-id="259e0-186">O MSXML geralmente relata um erro sobre a raiz não estar sendo definida corretamente se essa declaração de namespace estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="259e0-186">MSXML usually reports an error about the root not being properly defined if this namespace declaration is missing.</span></span>
  
## <a name="importing-and-including-schemas"></a><span data-ttu-id="259e0-187">Importando e incluindo esquemas</span><span class="sxs-lookup"><span data-stu-id="259e0-187">Importing and Including Schemas</span></span>

<span data-ttu-id="259e0-188">Os esquemas XSD são extensíveis e podem importar e incluir outros esquemas.</span><span class="sxs-lookup"><span data-stu-id="259e0-188">XSD schemas are extensible and can import and include other schemas.</span></span> <span data-ttu-id="259e0-189">Geralmente, você deve importar um esquema se o esquema especificado no atributo **targetNamespace** for diferente do esquema atual.</span><span class="sxs-lookup"><span data-stu-id="259e0-189">Generally, you should import a schema if the schema specified in the **targetNamespace** attribute differs from the current schema.</span></span> <span data-ttu-id="259e0-190">Você deve incluí-lo se o esquema especificado no atributo **targetNamespace** for o mesmo que o esquema atual.</span><span class="sxs-lookup"><span data-stu-id="259e0-190">You should include it if the schema specified in the **targetNamespace** attribute is the same as the current schema.</span></span> 
  
<span data-ttu-id="259e0-191">A semântica para importação e inclusão de esquemas é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="259e0-191">The semantics for importing and including schemas are as follows:</span></span>
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

<span data-ttu-id="259e0-192">Se o **atributo schemaLocation** estiver ausente (como acontece com alguns conversores), MSXML gera um erro porque não consegue encontrar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="259e0-192">If the **schemaLocation** attribute is missing (as happens with some converters), then MSXML raises an error because it cannot find the file.</span></span> <span data-ttu-id="259e0-193">Se você receber esse erro, verifique também se o recurso ou o local especificado no atributo schemaLocation está acessível pelos usuários do modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="259e0-193">If you get this error, also check to make sure that the resource or location specified in the schemaLocation attribute is accessible by users of the form template.</span></span> <span data-ttu-id="259e0-194">Obviamente, ocorrerão erros se o atributo **schemaLocation** fizer referência a um servidor ou diretório que está ino mesmo ou inexistente ou se os usuários não têm permissões de acesso.</span><span class="sxs-lookup"><span data-stu-id="259e0-194">Obviously, errors occur if the **schemaLocation** attribute references a server or directory that is down or nonexistent or if users do not have access permissions.</span></span> <span data-ttu-id="259e0-195">Além disso, examine todos os esquemas importados e incluídos para garantir que sejam válidos.</span><span class="sxs-lookup"><span data-stu-id="259e0-195">Also, be sure to examine all imported and included schemas to make sure they are valid.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="259e0-196">Erros causados por problemas com o **atributo schemaLocation** são um problema apenas quando o InfoPath importa os esquemas pela primeira vez; ou seja, quando você começa a criar um formulário com base em um esquema existente.</span><span class="sxs-lookup"><span data-stu-id="259e0-196">Errors caused by problems with the **schemaLocation** attribute are an issue only when InfoPath first imports the schemas; that is, when you first start designing a form based on an existing schema.</span></span> <span data-ttu-id="259e0-197">Depois disso, o InfoPath funciona com versões armazenadas em cache dos arquivos de esquema armazenados no modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="259e0-197">After that, InfoPath works with cached versions of the schema files that are stored in the form template.</span></span> 
  
<span data-ttu-id="259e0-198">Um atributo de namespace vazio é permitido ao importar um esquema, se esse esquema não especificar um **atributo targetNamespace.**</span><span class="sxs-lookup"><span data-stu-id="259e0-198">An empty namespace attribute is allowed when importing a schema, if that schema does not specify a **targetNamespace** attribute.</span></span> <span data-ttu-id="259e0-199">Em geral, o namespace na importação deve corresponder ao **targetNamespace** especificado no esquema que você importa.</span><span class="sxs-lookup"><span data-stu-id="259e0-199">In general, the namespace on the import must match the **targetNamespace** specified in the schema that you import.</span></span> 
  
## <a name="nondeterministic-schemas"></a><span data-ttu-id="259e0-200">Esquemas não determinísticos</span><span class="sxs-lookup"><span data-stu-id="259e0-200">Nondeterministic Schemas</span></span>

<span data-ttu-id="259e0-201">A infraestrutura MSXML 5.0 da qual o InfoPath depende pode detectar e aumentar erros de forma confiável para alertá-lo sobre esquemas não determinísticos, mas a mensagem de erro resultante não fornece um número de linha para dizer qual parte do esquema está aprindo o erro.</span><span class="sxs-lookup"><span data-stu-id="259e0-201">The MSXML 5.0 infrastructure that InfoPath depends upon can reliably detect and raise errors to alert you to nondeterministic schemas, but the resultant error message does not provide a line number to tell you which part of the schema is raising the error.</span></span> <span data-ttu-id="259e0-202">Esta seção discute por que é importante que os arquivos de esquema XSD sejam determinísticos e o que significa não ser determinístico.</span><span class="sxs-lookup"><span data-stu-id="259e0-202">This section discusses why it is important for XSD schema files to be deterministic and what it means to be nondeterministic.</span></span> <span data-ttu-id="259e0-203">Ele também mostra alguns erros comuns a evitar.</span><span class="sxs-lookup"><span data-stu-id="259e0-203">It also shows some common errors to avoid.</span></span>
  
<span data-ttu-id="259e0-204">Os esquemas XSD existem para validar a semântica de tipos e a estrutura de dados XML.</span><span class="sxs-lookup"><span data-stu-id="259e0-204">XSD schemas exist for the purpose of validating XML data structure and type semantics.</span></span> <span data-ttu-id="259e0-205">Para realizar essa tarefa, o sistema de validação (neste caso, MSXML 5.0) deve mapear nós XML para declarações XSD.</span><span class="sxs-lookup"><span data-stu-id="259e0-205">To accomplish this task, the validating system (in this case, MSXML 5.0) must map XML nodes to XSD declarations.</span></span> <span data-ttu-id="259e0-206">Sem esse mapeamento, o sistema de validação não pode realizar sua tarefa.</span><span class="sxs-lookup"><span data-stu-id="259e0-206">Without this mapping, the validating system cannot accomplish its task.</span></span> <span data-ttu-id="259e0-207">Se um mapeamento puder ser garantido, o esquema será determinístico.</span><span class="sxs-lookup"><span data-stu-id="259e0-207">If a mapping can be guaranteed, then the schema is deterministic.</span></span> <span data-ttu-id="259e0-208">Se houver uma única instância XML que torna esse mapeamento impossível, o esquema não é determinístico.</span><span class="sxs-lookup"><span data-stu-id="259e0-208">If there is a single XML instance that makes this mapping impossible, then the schema is nondeterministic.</span></span>
  
<span data-ttu-id="259e0-209">O esquema de exemplo a seguir não é determinístico:</span><span class="sxs-lookup"><span data-stu-id="259e0-209">The following example schema is nondeterministic:</span></span>
  
```XML
<xsd:element name="file_Information"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element name="file_name"/> 
            <xsd:choice> 
                <xsd:element name="file_path"/> 
                <xsd:sequence> 
                    <xsd:element name="file_path" minOccurs="0"/> 
                    <xsd:element name="URI"/> 
                </xsd:sequence> 
            </xsd:choice> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="259e0-210">Para ilustrar por que esse segmento XSD não é determinístico, suponha que você tenha o fragmento XML a seguir que deseja validar com este esquema:</span><span class="sxs-lookup"><span data-stu-id="259e0-210">To illustrate why this XSD segment is nondeterministic, assume you have the following XML fragment that you want to validate with this schema:</span></span>
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

<span data-ttu-id="259e0-211">Nesse fragmento XML, não está claro se o elemento *\< file_path \>* é o nó necessário da primeira parte da declaração de escolha ou o opcional da segunda parte da declaração de escolha.</span><span class="sxs-lookup"><span data-stu-id="259e0-211">In this XML fragment, it is not clear whether the  *\<file_path\>*  element is the required node from the first part of the choice declaration or the optional one from the second part of the choice declaration.</span></span> <span data-ttu-id="259e0-212">Essa distinção é importante pelos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="259e0-212">This distinction is important for the following reasons:</span></span> 
  
1. <span data-ttu-id="259e0-213">Se o fragmento XML for validado em relação à primeira parte da declaração de escolha, o XML será válido em relação ao esquema.</span><span class="sxs-lookup"><span data-stu-id="259e0-213">If the XML fragment is validated against the first part of the choice declaration, then the XML is valid against the schema.</span></span>
    
2. <span data-ttu-id="259e0-214">Se o fragmento XML for validado em relação à segunda parte da declaração de escolha, o esquema não será válido, pois o nó \< de URI \> necessário está ausente.</span><span class="sxs-lookup"><span data-stu-id="259e0-214">If the XML fragment is validated against the second part of the choice declaration, then the schema is not valid, because the required \<URI\> node is missing.</span></span> 
    
<span data-ttu-id="259e0-215">Alguns sistemas de validação XSD erram em relação à validação desse esquema porque há um caminho válido.</span><span class="sxs-lookup"><span data-stu-id="259e0-215">Some XSD validation systems err toward validating against this schema because there is a valid path.</span></span> <span data-ttu-id="259e0-216">O MSXML é mais estrito e gera um erro informando que o esquema não é determinístico.</span><span class="sxs-lookup"><span data-stu-id="259e0-216">MSXML is stricter and raises an error stating that the schema is nondeterministic.</span></span>
  
<span data-ttu-id="259e0-217">A seguir estão alguns exemplos de esquemas não determinísticos.</span><span class="sxs-lookup"><span data-stu-id="259e0-217">What follows are a few more examples of nondeterministic schemas.</span></span> <span data-ttu-id="259e0-218">A primeira lida com elementos opcionais.</span><span class="sxs-lookup"><span data-stu-id="259e0-218">The first deals with optional elements.</span></span> <span data-ttu-id="259e0-219">Esses casos geralmente surgem de XDR para conversores XSD devido a diferenças nas cardinalidades padrão nas duas linguagens de esquema.</span><span class="sxs-lookup"><span data-stu-id="259e0-219">These cases often arise from XDR to XSD converters because of differences in the default cardinalities in the two schema languages.</span></span> <span data-ttu-id="259e0-220">O primeiro caso a ser considerado são elementos opcionais declarados com **elementos xsd:choice** e **xsd:sequence.**</span><span class="sxs-lookup"><span data-stu-id="259e0-220">The first case to consider is optional elements declared with **xsd:choice** and **xsd:sequence** elements.</span></span> <span data-ttu-id="259e0-221">Elementos opcionais declarados em um elemento **xsd:sequence** geralmente são validados corretamente, desde que você não tenha elementos com o mesmo nome mais de uma vez, com apenas elementos opcionais entre eles.</span><span class="sxs-lookup"><span data-stu-id="259e0-221">Optional elements declared in an **xsd:sequence** element usually validate properly, as long as you do not have elements with the same name more than once, with only optional elements in between.</span></span> <span data-ttu-id="259e0-222">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="259e0-222">For example:</span></span> 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:element ref="aNode" /> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="259e0-223">Para entender por que esse segmento de esquema não é determinístico, suponha que você tenha o seguinte fragmento XML inválido:</span><span class="sxs-lookup"><span data-stu-id="259e0-223">To understand why this schema segment is nondeterministic, assume you have the following invalid XML fragment:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
    <anotherNode/> 
</container> 

```

<span data-ttu-id="259e0-224">Ao olhar para esse fragmento, você pode ver por que ele é inválido: há dois elementos antes do elemento, quando  `<aNode>` apenas um é  `<anotherNode>` permitido.</span><span class="sxs-lookup"><span data-stu-id="259e0-224">Looking at this fragment, you can see why it is invalid: there are two  `<aNode>` elements before the  `<anotherNode>` element, when only one is allowed.</span></span> 
  
<span data-ttu-id="259e0-225">Agora, suponha que você tenha a seguinte instância XML para validar:</span><span class="sxs-lookup"><span data-stu-id="259e0-225">Now assume that you have the following XML instance to validate:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

<span data-ttu-id="259e0-226">O desafio é determinar se essa instância é válida.</span><span class="sxs-lookup"><span data-stu-id="259e0-226">The challenge is to determine whether this instance is valid.</span></span> <span data-ttu-id="259e0-227">Você tem dois elementos onde apenas um é permitido ou você tem um elemento onde ele é permitido e  `<aNode>` outro onde ele é  `<aNode>` permitido?</span><span class="sxs-lookup"><span data-stu-id="259e0-227">Do you have two  `<aNode>` elements where only one is allowed, or do you have an  `<aNode>` element where it is allowed and another where it is allowed?</span></span> <span data-ttu-id="259e0-228">O esquema não é determinístico porque não há como saber.</span><span class="sxs-lookup"><span data-stu-id="259e0-228">The schema is nondeterministic because there is no way to know.</span></span> 
  
<span data-ttu-id="259e0-229">Da mesma forma, elementos opcionais declarados em um **elemento xsd:choice** geralmente são problemáticos.</span><span class="sxs-lookup"><span data-stu-id="259e0-229">Similarly, optional elements declared in an **xsd:choice** element are usually problematic.</span></span> <span data-ttu-id="259e0-230">No exemplo simplificado a seguir, não há nenhuma maneira de determinar se a escolha ocorreu uma vez com o elemento opcional não estando lá ou se ela nunca ocorreu.</span><span class="sxs-lookup"><span data-stu-id="259e0-230">In the following simplified example, there is no way to determine whether the choice occurred once with the optional element not being there or whether it never occurred at all.</span></span> 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

<span data-ttu-id="259e0-231">A prática questionável final é usar um **elemento xsd:any** sem uma definição de namespace, como em , após um `<xsd:any namespace="##other"/>` elemento **xsd:sequence.**</span><span class="sxs-lookup"><span data-stu-id="259e0-231">The final questionable practice is using an **xsd:any** element without a namespace definition, as in  `<xsd:any namespace="##other"/>` , after an **xsd:sequence** element.</span></span> <span data-ttu-id="259e0-232">Essa construção é especialmente problemática quando segue um elemento opcional.</span><span class="sxs-lookup"><span data-stu-id="259e0-232">This construct is especially troublesome when it follows an optional element.</span></span> <span data-ttu-id="259e0-233">Se você revisitar o exemplo anterior e alterar apenas o último nó para um elemento **xsd:any,** poderá ver que todos os argumentos anteriores sobre nondeterminismo ainda se aplicam, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="259e0-233">If you revisit the previous example and change just the last node to an **xsd:any** element, you can see that all the previous arguments about nondeterminism still apply, as follows:</span></span> 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:any />     
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="illegal-enumeration-values"></a><span data-ttu-id="259e0-234">Valores de enumeração ilegais</span><span class="sxs-lookup"><span data-stu-id="259e0-234">Illegal Enumeration Values</span></span>

<span data-ttu-id="259e0-235">Esquemas XSD normalmente não executam nenhuma validação de tipo até que você valide um documento de instância real.</span><span class="sxs-lookup"><span data-stu-id="259e0-235">XSD schemas typically do not perform any type validation until you validate an actual instance document.</span></span> <span data-ttu-id="259e0-236">Uma exceção a isso é quando você tem uma enumeração em seu esquema.</span><span class="sxs-lookup"><span data-stu-id="259e0-236">An exception to this is when you have an enumeration in your schema.</span></span> <span data-ttu-id="259e0-237">Nesse caso, o esquema valida os valores de enumeração em relação aos tipos de enumeração para garantir que sejam valores de nó adequados.</span><span class="sxs-lookup"><span data-stu-id="259e0-237">In this case, the schema validates the enumeration values against the enumeration types to ensure they are proper node values.</span></span> <span data-ttu-id="259e0-238">Aqui estão dois exemplos:</span><span class="sxs-lookup"><span data-stu-id="259e0-238">Here are two examples:</span></span>
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="259e0-239">Esse esquema é inválido porque "horário da manhã" não é um valor válido para um elemento do tipo **xsd:time**.</span><span class="sxs-lookup"><span data-stu-id="259e0-239">This schema is invalid because "eleven o'clock" is not a valid value for an element of type **xsd:time**.</span></span>
  
<span data-ttu-id="259e0-240">Veja a seguir um exemplo mais complexo:</span><span class="sxs-lookup"><span data-stu-id="259e0-240">The following is a more complex example:</span></span>
  
```XML
<xsd:simpleType name="concession"> 
    <xsd:restriction base="xsd:NMTOKEN"> 
        <xsd:enumeration value="GummyBears"/> 
        <xsd:enumeration value="SnowCaps"/> 
        <xsd:enumeration value="M&Ms"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="259e0-241">Para entender por que este exemplo é inválido, você deve entender como o tipo **xsd:NMTOKEN** é definido.</span><span class="sxs-lookup"><span data-stu-id="259e0-241">To understand why this example is invalid, you must understand how the type **xsd:NMTOKEN** is defined.</span></span> <span data-ttu-id="259e0-242">A especificação de tipos de dados W3C define o tipo **NMTOKEN** da seguinte forma: "Um NMTOKEN (token de nome) é qualquer mistura de caracteres de nome".</span><span class="sxs-lookup"><span data-stu-id="259e0-242">The W3C data types specification defines the **NMTOKEN** type as follows: "An NMTOKEN (name token) is any mixture of name characters."</span></span> 
  
<span data-ttu-id="259e0-243">Se você investigar mais, descobrirá que "&" não é um caractere de nome válido e, portanto, "M&Ms" não valida como um tipo **NMTOKEN.**</span><span class="sxs-lookup"><span data-stu-id="259e0-243">If you investigate further, you find that '&' is not a valid name character, and therefore "M&Ms" does not validate as an **NMTOKEN** type.</span></span> 
  
## <a name="empty-sequence-or-choice-elements"></a><span data-ttu-id="259e0-244">Elementos de sequência ou escolha vazios</span><span class="sxs-lookup"><span data-stu-id="259e0-244">Empty Sequence or Choice Elements</span></span>

<span data-ttu-id="259e0-245">Às vezes, o MSXML gera erros sobre declarações de esquema que contêm elementos **xsd:choice** ou **xsd:sequence** vazios, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="259e0-245">MSXML sometimes raises errors about schema declarations that contain empty **xsd:choice** or **xsd:sequence** elements, as shown in the following example.</span></span> 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="259e0-246">Remover a marca  `<xsd:choice />` vazia deve resolver esse problema.</span><span class="sxs-lookup"><span data-stu-id="259e0-246">Removing the empty  `<xsd:choice />` tag should resolve this problem.</span></span> 
  
## <a name="regular-expressions"></a><span data-ttu-id="259e0-247">Expressões Regulares</span><span class="sxs-lookup"><span data-stu-id="259e0-247">Regular Expressions</span></span>

<span data-ttu-id="259e0-248">O MSXML 5.0 pode ter problemas para validar padrões de expressões regulares durante o carregamento.</span><span class="sxs-lookup"><span data-stu-id="259e0-248">MSXML 5.0 can have problems validating regular expression patterns on load.</span></span> <span data-ttu-id="259e0-249">Expressões regulares podem ser complicadas e você deve ter cuidado ao usá-las.</span><span class="sxs-lookup"><span data-stu-id="259e0-249">Regular expressions can be complicated, and you should be careful when you are using them.</span></span> <span data-ttu-id="259e0-250">Cada analisador XSD parece ter linguagens de expressões regulares flexíveis; ou seja, eles implementam a linguagem oficial de expressão regular XSD, além de elementos de outras linguagens de expressão regular.</span><span class="sxs-lookup"><span data-stu-id="259e0-250">Every XSD parser seems to have flexible regular expression languages; that is, they implement the official XSD regular expression language plus elements from other regular expression languages.</span></span> <span data-ttu-id="259e0-251">Se o designer de formulário do InfoPath tiver problemas para analisar uma expressão regular, os dados de exemplo gerados pelo InfoPath poderão ser inválidos ou podem não ser gerados.</span><span class="sxs-lookup"><span data-stu-id="259e0-251">If InfoPath form designer has problems parsing a regular expression, then the sample data InfoPath generates might be invalid or might not be generated at all.</span></span> <span data-ttu-id="259e0-252">Isso é aceitável no tempo de design, pois o InfoPath usa apenas dados de exemplo para formatação.</span><span class="sxs-lookup"><span data-stu-id="259e0-252">This is acceptable at design time, because InfoPath uses only sample data for formatting.</span></span> <span data-ttu-id="259e0-253">No entanto, se você usar uma expressão regular que o MSXML não suporta, o InfoPath não poderá validar um valor em relação a ele quando um usuário estiver preenchendo um formulário.</span><span class="sxs-lookup"><span data-stu-id="259e0-253">However, if you use a regular expression that MSXML does not support, then InfoPath cannot validate a value against it when a user is filling out a form.</span></span> <span data-ttu-id="259e0-254">[Xml Schema Part 0: Primer Second Edition](https://www.w3.org/TR/xmlschema-0/)describes what is supported in XSD regular expressions.</span><span class="sxs-lookup"><span data-stu-id="259e0-254">[XML Schema Part 0: Primer Second Edition](https://www.w3.org/TR/xmlschema-0/)describes what is supported in XSD regular expressions.</span></span> <span data-ttu-id="259e0-255">Para obter mais informações sobre expressões regulares XSD e expressões regulares Unicode nível 1, consulte [Expressões regulares Unicode.](https://www.unicode.org/reports/tr18/)</span><span class="sxs-lookup"><span data-stu-id="259e0-255">For more information about XSD regular expressions and Unicode level 1 regular expressions, see [Unicode Regular Expressions](https://www.unicode.org/reports/tr18/) .</span></span> 
  
## <a name="targetnamespace-attribute-issues"></a><span data-ttu-id="259e0-256">Problemas de atributo targetNamespace</span><span class="sxs-lookup"><span data-stu-id="259e0-256">targetNamespace Attribute Issues</span></span>

<span data-ttu-id="259e0-257">O XSD é interessante porque, por padrão, o atributo **targetNamespace** refere-se apenas às declarações de nível superior, embora você possa definir e substituir esse  `attributeFormDefault=qualified`  `elementFormDefault=qualified` comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="259e0-257">XSD is interesting in that, by default, the **targetNamespace** attribute refers to only the top-level declarations, although you can set  `attributeFormDefault=qualified` and  `elementFormDefault=qualified` to override this default behavior.</span></span> <span data-ttu-id="259e0-258">Por exemplo, suponha que você tenha o seguinte XSD.</span><span class="sxs-lookup"><span data-stu-id="259e0-258">As an example, assume that you have the following XSD.</span></span> 
  
```XML
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema" targetNamespace="https://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element name="local"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
</xsd:schema> 

```

<span data-ttu-id="259e0-259">E que seu documento de instância XML se parece com o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="259e0-259">And that, your XML instance document resembles the following example.</span></span>
  
```XML
<ns:root xmlns:ns="https://ns"> 
    <local/> 
</ns:root> 

```

<span data-ttu-id="259e0-260">As definições locais não exigem o namespace de destino porque a qualificação está desligada por padrão.</span><span class="sxs-lookup"><span data-stu-id="259e0-260">Local definitions do not require the target namespace because qualification is turned off by default.</span></span> <span data-ttu-id="259e0-261">No entanto, se você alterar sua definição local para global, sua referência deverá ser qualificada com o prefixo de namespace.</span><span class="sxs-lookup"><span data-stu-id="259e0-261">However, if you change your local definition to be global, then your reference must be qualified with the namespace prefix.</span></span> <span data-ttu-id="259e0-262">Por exemplo, o esquema a seguir é inválido.</span><span class="sxs-lookup"><span data-stu-id="259e0-262">For example, the following schema is invalid.</span></span>
  
```XML
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema" targetNamespace="https://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

<span data-ttu-id="259e0-263">Esse esquema é inválido porque "global" está no namespace " https://ns ".</span><span class="sxs-lookup"><span data-stu-id="259e0-263">This schema is invalid because "global" is in the namespace "https://ns".</span></span> <span data-ttu-id="259e0-264">O ref="global" simples não é reconhecido porque o namespace padrão não é " https://ns ".</span><span class="sxs-lookup"><span data-stu-id="259e0-264">The simple ref="global" is not recognized because the default namespace is not "https://ns".</span></span> <span data-ttu-id="259e0-265">Para corrigir isso, você deve adicionar um prefixo para o namespace de destino e usá-lo para todas as referências globais e usos de tipo.</span><span class="sxs-lookup"><span data-stu-id="259e0-265">To fix this, you must add a prefix for the target namespace and use that for all global references and type uses.</span></span> <span data-ttu-id="259e0-266">O esquema corrigido é parecido com o seguinte.</span><span class="sxs-lookup"><span data-stu-id="259e0-266">The corrected schema looks like the following.</span></span>
  
```XML
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
    xmlns:ns="https://ns" targetNamespace="https://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="ns:global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

<span data-ttu-id="259e0-267">Se o esquema tiver o **atributo targetNamespace** especificado, certifique-se de que todas as referências globais sejam qualificadas com o prefixo de namespace correto.</span><span class="sxs-lookup"><span data-stu-id="259e0-267">If your schema has the **targetNamespace** attribute specified, ensure that all global references are qualified with the correct namespace prefix.</span></span> 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a><span data-ttu-id="259e0-268">Codificação de instrução de processamento XML (Unicode versus ANSII)</span><span class="sxs-lookup"><span data-stu-id="259e0-268">XML Processing Instruction Encoding (Unicode vs. ANSII)</span></span>

<span data-ttu-id="259e0-269">XML oferece suporte apenas a conjuntos de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="259e0-269">XML supports only Unicode character sets.</span></span> <span data-ttu-id="259e0-270">Portanto, você pode perder informações se salvar arquivos que usam caracteres ANSII.</span><span class="sxs-lookup"><span data-stu-id="259e0-270">Therefore, you may lose information if you save files that use ANSII characters.</span></span> <span data-ttu-id="259e0-271">No entanto, salvar arquivos como UTF-16 pode ser excessivo para seu uso específico.</span><span class="sxs-lookup"><span data-stu-id="259e0-271">However, saving files as UTF-16 may be excessive for your particular use.</span></span> <span data-ttu-id="259e0-272">Para reduzir o custo de implementação de um leitor de XML, o autor xml deve dizer qual codificação eles estão usando na instrução de processamento XML de nível superior.</span><span class="sxs-lookup"><span data-stu-id="259e0-272">To reduce the implementation cost of an XML reader, the XML author must state which encoding they are using in the top-level XML processing instruction.</span></span> <span data-ttu-id="259e0-273">Você pode reconhecer a instrução de processamento a seguir.</span><span class="sxs-lookup"><span data-stu-id="259e0-273">You may recognize the following processing instruction.</span></span>
  
```XML
xml version="1.0" encoding="UTF-8"
```

<span data-ttu-id="259e0-274">Essa marca de instrução de processamento especifica que a codificação do arquivo é UTF-8.</span><span class="sxs-lookup"><span data-stu-id="259e0-274">This processing instruction tag specifies that the encoding of the file is UTF-8.</span></span> <span data-ttu-id="259e0-275">Você deve garantir que a codificação do arquivo seja a mesma que a codificação indicado na marca de instrução de processamento.</span><span class="sxs-lookup"><span data-stu-id="259e0-275">You must ensure that the file encoding is the same as the encoding stated in the processing instruction tag.</span></span> <span data-ttu-id="259e0-276">Você pode determinar a codificação observando os bytes do arquivo e procurando as marcas de ordem de bytes Unicode.</span><span class="sxs-lookup"><span data-stu-id="259e0-276">You can determine the encoding by looking at the bytes of the file and looking for the Unicode byte order marks.</span></span> <span data-ttu-id="259e0-277">Mas há uma maneira mais fácil.</span><span class="sxs-lookup"><span data-stu-id="259e0-277">But there is an easier way.</span></span> <span data-ttu-id="259e0-278">Se você tiver problemas para abrir um esquema XSD, especifique a codificação como "UTF-8", abra-a em um editor de texto como o  Bloco de Notas e salve  o arquivo usando a codificação UTF-8 (o Bloco de Notas fornece a lista de codificação na caixa de diálogo Salvar como).</span><span class="sxs-lookup"><span data-stu-id="259e0-278">If you have problems opening an XSD schema, specify the encoding as "UTF-8", open it in a text editor such as Notepad, and then save the file by using UTF-8 encoding (Notepad provides the **Encoding** drop-down list in the **Save As** dialog box).</span></span> <span data-ttu-id="259e0-279">Se você ainda tiver problemas para abrir o arquivo, não será um problema de codificação.</span><span class="sxs-lookup"><span data-stu-id="259e0-279">If you still have problems opening the file, it is not an encoding issue.</span></span> 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a><span data-ttu-id="259e0-280">Atributo maxOccurs dentro do elemento xsd:all</span><span class="sxs-lookup"><span data-stu-id="259e0-280">maxOccurs Attribute Inside the xsd:all Element</span></span>

<span data-ttu-id="259e0-281">Devido à maneira como o nondeterminismo é definido na recomendação de esquema XML, o único valor válido para o atributo **maxOccurs** de um elemento **xsd:element** dentro de um elemento **xsd:all** é 1.</span><span class="sxs-lookup"><span data-stu-id="259e0-281">Due to the way nondeterminism is defined in the XML Schema recommendation, the only valid value for the **maxOccurs** attribute of an **xsd:element** element inside an **xsd:all** element is 1.</span></span> <span data-ttu-id="259e0-282">Por exemplo, o seguinte é válido.</span><span class="sxs-lookup"><span data-stu-id="259e0-282">For example, the following is valid.</span></span> 
  
```XML
<xsd:all> 
    <xsd:element name="x" minOccurs="0"/> 
    <xsd:element name="docs" minOccurs="0"/> 
</xsd:all> 

```

<span data-ttu-id="259e0-283">No entanto, este exemplo não é válido.</span><span class="sxs-lookup"><span data-stu-id="259e0-283">However, this example is not valid.</span></span>
  
```XML
<xsd:all>     
    <xsd:element name="x" minOccurs="0" maxOccurs="unbounded"/> 
    <xsd:element name="docs" minOccurs="0" maxOccurs="unbounded"/> 
</xsd:all> 

```

<span data-ttu-id="259e0-284">Este exemplo é inválido porque o sistema de validação não pode determinar se duas ocorrências de mapa para a declaração única ou para a declaração  `<x/>` e outra definição inválida.</span><span class="sxs-lookup"><span data-stu-id="259e0-284">This example is invalid because the validation system cannot determine whether two occurrences of  `<x/>` map to the single declaration or to the declaration and another invalid definition.</span></span> <span data-ttu-id="259e0-285">Nas mesmas linhas, não é possível ter dois elementos com o mesmo nome em uma  `<xsd:all>` marca.</span><span class="sxs-lookup"><span data-stu-id="259e0-285">Along the same lines, you cannot have two elements of the same name in an  `<xsd:all>` tag.</span></span> 
  
<span data-ttu-id="259e0-286">Este exemplo também é interessante porque permite que você tenha qualquer número de nós dentro de um elemento que o contém  `<x/>`  `<docs/>` em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="259e0-286">This example is also interesting because it allows you to have any number of  `<x/>` and  `<docs/>` nodes inside a containing element in any order.</span></span> <span data-ttu-id="259e0-287">Embora essa construção seja inválida, há uma solução alternativa.</span><span class="sxs-lookup"><span data-stu-id="259e0-287">Although this construct is invalid, there is a workaround.</span></span> <span data-ttu-id="259e0-288">Usando o **elemento xsd:choice,** você pode obter o mesmo resultado, conforme demonstrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="259e0-288">By using the **xsd:choice** element, you can achieve the same result, as demonstrated in the following example.</span></span> 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a><span data-ttu-id="259e0-289">Como editar ou editar um XSD para InfoPath</span><span class="sxs-lookup"><span data-stu-id="259e0-289">How to Edit or Author an XSD for InfoPath</span></span>

<span data-ttu-id="259e0-290">Os dois exemplos nas seções a seguir mostram como editar ou gerar um esquema para produzir resultados específicos no InfoPath.</span><span class="sxs-lookup"><span data-stu-id="259e0-290">The two examples in the following sections show how to edit or author a schema to produce specific results in InfoPath.</span></span>
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a><span data-ttu-id="259e0-291">Permitindo que elementos definidos pelo usuário sejam inseridos no painel de tarefas Fields</span><span class="sxs-lookup"><span data-stu-id="259e0-291">Allowing User-defined Elements to Be Inserted in the Fields Task Pane</span></span>

<span data-ttu-id="259e0-292">Para permitir que elementos definidos pelo usuário apareçam em um elemento pai no painel de tarefas **Fields,** você deve inserir um elemento **xsd:any** sob o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="259e0-292">To allow user-defined elements to appear under a parent element in the **Fields** task pane, you must insert an **xsd:any** element under the parent element.</span></span> <span data-ttu-id="259e0-293">Para permitir que elementos definidos pelo usuário sejam inseridos dentro , a declaração  `<your_node_name>` XSD deve se parecer com o seguinte.</span><span class="sxs-lookup"><span data-stu-id="259e0-293">To allow user-defined elements to be inserted inside  `<your_node_name>` , the XSD declaration should resemble the following.</span></span> 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="##any | ##other"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="259e0-294">Se você também quiser permitir atributos definidos pelo usuário, deverá adicionar  `<xsd:anyAttribute namespace="##any | ##other"/>` à declaração do elemento.</span><span class="sxs-lookup"><span data-stu-id="259e0-294">If you also want to allow user-defined attributes, then you must add  `<xsd:anyAttribute namespace="##any | ##other"/>` to the element declaration.</span></span> 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a><span data-ttu-id="259e0-295">Permitindo que elementos rich text sejam vinculados em modos de edição e design do InfoPath</span><span class="sxs-lookup"><span data-stu-id="259e0-295">Allowing Rich Text Elements to be Bound in InfoPath Design and Edit Modes</span></span>

<span data-ttu-id="259e0-296">Se você deseja declarar um elemento que pode ser vinculado a um controle **Rich Text Box,** ele deve ter o seguinte formulário, que inclui o elemento **xsd:any** que tem um atributo de namespace definido como " " conforme mostrado no exemplo a https://www.w3.org/1999/xhtml seguir.</span><span class="sxs-lookup"><span data-stu-id="259e0-296">If you want to declare an element that can be bound to a **Rich Text Box** control, then it should have the following form, which includes the **xsd:any** element that has a namespace attribute set to "https://www.w3.org/1999/xhtml" as shown in the following example.</span></span> 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="https://www.w3.org/1999/xhtml"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="conclusion"></a><span data-ttu-id="259e0-297">Conclusão</span><span class="sxs-lookup"><span data-stu-id="259e0-297">Conclusion</span></span>

<span data-ttu-id="259e0-298">Ao aproveitar o suporte do InfoPath para projetar soluções de formulário XML baseadas em arquivos de esquema XML (.xsd) criados externamente, você pode criar um modelo de formulário que funciona com um esquema padrão do setor ou um esquema personalizado criado por sua empresa ou organização.</span><span class="sxs-lookup"><span data-stu-id="259e0-298">By taking advantage of InfoPath support for designing XML form solutions that are based on externally authored XML Schema (.xsd) files, you can create a form template that works with an industry-standard schema or custom schema created by your company or organization.</span></span> <span data-ttu-id="259e0-299">Usando as informações deste artigo, você pode criar arquivos de esquema XSD personalizados compatíveis com o InfoPath e solucionar problemas comuns que você pode encontrar ao carregar arquivos XSD criado externamente no ambiente de design do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="259e0-299">By using the information in this article, you can create custom XSD schema files that are compatible with InfoPath, and you can troubleshoot common issues that you may encounter when you load externally authored XSD files into the InfoPath design environment.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="259e0-300">Confira também</span><span class="sxs-lookup"><span data-stu-id="259e0-300">See also</span></span>

- [<span data-ttu-id="259e0-301">Esquema XML W3C</span><span class="sxs-lookup"><span data-stu-id="259e0-301">W3C XML Schema</span></span>](https://www.w3.org/XML/Schema)
- [<span data-ttu-id="259e0-302">Manual de esquema XML W3C</span><span class="sxs-lookup"><span data-stu-id="259e0-302">W3C XML Schema Primer</span></span>](https://www.w3.org/TR/xmlschema-0/)
- [<span data-ttu-id="259e0-303">Referência de estruturas de esquema XML W3C</span><span class="sxs-lookup"><span data-stu-id="259e0-303">W3C XML Schema Structures Reference</span></span>](https://www.xml.com/pub/a/2000/11/29/schemas/structuresref.html)
- [<span data-ttu-id="259e0-304">Referência de datatypes de esquema XML W3C</span><span class="sxs-lookup"><span data-stu-id="259e0-304">W3C XML Schema Datatypes Reference</span></span>](https://www.xml.com/pub/a/2000/11/29/schemas/dataref.html)
- [<span data-ttu-id="259e0-305">Tutorial de esquema XML</span><span class="sxs-lookup"><span data-stu-id="259e0-305">XML Schema Tutorial</span></span>](https://www.w3schools.com/xml/schema_intro.asp)
- [<span data-ttu-id="259e0-306">Central de Desenvolvedores XML</span><span class="sxs-lookup"><span data-stu-id="259e0-306">XML Developer Center</span></span>](https://msdn.microsoft.com/xml/default.aspx)

