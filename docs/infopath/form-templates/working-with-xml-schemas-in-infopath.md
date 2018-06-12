---
title: Trabalhando com esquemas XML no InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c1d70e9f-b9fc-7bdb-107e-d0cd8191607b
description: Um modelo de formulário que você criou com o Microsoft InfoPath usa um esquema XML (XSD) para executar estrutural e validação de dados em XML que é de entrada, editado, e a saída de um formulário do InfoPath. Cada modelo de formulário criado no InfoPath form designer contém pelo menos um arquivo de esquema XSD (. xsd) que é usado para validação em tempo de execução.
ms.openlocfilehash: 6921a2206c098992a0a24e85c263992a0e2c98b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765730"
---
# <a name="working-with-xml-schemas-in-infopath"></a><span data-ttu-id="1ec9a-104">Trabalhando com esquemas XML no InfoPath</span><span class="sxs-lookup"><span data-stu-id="1ec9a-104">Working with XML Schemas in InfoPath</span></span>

<span data-ttu-id="1ec9a-105">Um modelo de formulário que você criou com o Microsoft InfoPath usa um esquema XML (XSD) para executar estrutural e validação de dados em XML que é de entrada, editado, e a saída de um formulário do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-105">A form template that you create with Microsoft InfoPath uses an XML Schema (XSD) to perform structural and data validation on the XML that is input, edited, and output from an InfoPath form.</span></span> <span data-ttu-id="1ec9a-106">Cada modelo de formulário criado no InfoPath form designer contém pelo menos um arquivo de esquema XSD (. xsd) que é usado para validação em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-106">Every form template created in the InfoPath form designer contains at least one XSD schema file (.xsd) that is used for validation at run time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1ec9a-107">As informações contidas neste tópico se aplica a modelos de formulários projetados para uso no editor do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-107">The information contained in this topic applies to form templates designed for use in the InfoPath editor.</span></span> <span data-ttu-id="1ec9a-108">Modelos de formulário compatíveis com navegador têm requisitos de esquema XSD mais restritas.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-108">Browser-compatible form templates have stricter XSD Schema requirements.</span></span> <span data-ttu-id="1ec9a-109">Para obter mais informações, consulte a documentação sobre esquemas XML em modelos de formulário compatíveis com navegador disponíveis no MSDN.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-109">For more information, see the documentation about XML Schemas in browser-compatible form templates available on MSDN.</span></span> 
  
## <a name="using-externally-authored-xml-schemas"></a><span data-ttu-id="1ec9a-110">Usando esquemas XML criados externamente</span><span class="sxs-lookup"><span data-stu-id="1ec9a-110">Using Externally-authored XML Schemas</span></span>

<span data-ttu-id="1ec9a-111">Para carregar um arquivo de esquema XSD que foi criado fora do InfoPath, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-111">To load an XSD schema file that was authored outside of InfoPath, follow these steps.</span></span>
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a><span data-ttu-id="1ec9a-112">Para criar um modelo de formulário baseado em um esquema externo</span><span class="sxs-lookup"><span data-stu-id="1ec9a-112">To create a form template based on an external schema</span></span>

1. <span data-ttu-id="1ec9a-113">No Backstage, clique em **novo**, clique **XML ou esquema** em **Modelos de formulário avançado**e, em seguida, clique em **Criar este formulário**.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-113">In the Backstage, click **New**, click **XML or Schema** under **Advanced Form Templates**, and then click **Design This Form**.</span></span>
    
2. <span data-ttu-id="1ec9a-114">No **Assistente de fonte de dados**, especifique o arquivo de esquema XSD que você deseja usar e clique em **Avançar** e conclua as páginas restantes do assistente.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-114">In the **Data Source Wizard**, specify the XSD schema file you want to use, and then click **Next** and complete the remaining pages of the wizard.</span></span> 
    
## <a name="unsupported-xsd-constructs"></a><span data-ttu-id="1ec9a-115">Construções XSD sem suporte</span><span class="sxs-lookup"><span data-stu-id="1ec9a-115">Unsupported XSD Constructs</span></span>

<span data-ttu-id="1ec9a-116">As seções a seguir descrevem construções XSD quais InfoPath não dá suporte em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-116">The following sections describe XSD constructs that InfoPath cannot handle at run time.</span></span> <span data-ttu-id="1ec9a-117">Evite essas construções ao criar um modelo de formulário no designer de formulários do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-117">Avoid these constructs when creating a form template in the InfoPath form designer.</span></span>
  
## <a name="entity-and-entities-types"></a><span data-ttu-id="1ec9a-118">ENTIDADE e tipos de ENTIDADES</span><span class="sxs-lookup"><span data-stu-id="1ec9a-118">ENTITY and ENTITIES Types</span></span>

<span data-ttu-id="1ec9a-119">Os tipos de **entidade** e **ENTIDADES** exigem uma definição de tipo de documento (DTD) para validação, que não dá suporte ao InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-119">The **ENTITY** and **ENTITIES** types require a document type definition (DTD) for validation, which InfoPath does not support.</span></span> <span data-ttu-id="1ec9a-120">O InfoPath não permite a criação de um modelo de formulário com um esquema tal e exibe uma mensagem de erro que recomenda alterar o tipo de **entidade** para o tipo de **NCName** do qual deriva de **entidade** .</span><span class="sxs-lookup"><span data-stu-id="1ec9a-120">InfoPath does not allow you to design a form template against such a schema and displays an error message that recommends changing the **ENTITY** type to the **NCName** type from which **ENTITY** derives.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="1ec9a-121">Se você cria manualmente um modelo de formulário do InfoPath fora do modo de design e ele usa um XSD que inclui os tipos de **entidade** e **ENTIDADES** , o modelo de formulário pode funcionar em tempo de execução se o arquivo de Template contiver o DTD necessário para esses tipos.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-121">If you manually author an InfoPath form template outside of design mode, and it uses an XSD that includes **ENTITY** and **ENTITIES** types, the form template may work at run time if the Template.xml file contains the required DTD for these types.</span></span> 
  
## <a name="required-xsdany-element"></a><span data-ttu-id="1ec9a-122">Obrigatório xsd: qualquer elemento</span><span class="sxs-lookup"><span data-stu-id="1ec9a-122">Required xsd:any Element</span></span>

<span data-ttu-id="1ec9a-123">Uma ocorrência de um **xsd: qualquer** elemento curinga, ou seja, uma ocorrência de um **xsd: qualquer** elemento com um valor de atributo **minOccurs** maior do que zero ("obrigatório qualquer"), impede que o InfoPath forma determinista criando uma instância válida de Esse fragmento de esquema.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-123">An occurrence of an **xsd:any** wildcard element, that is, an occurrence of an **xsd:any** element with a **minOccurs** attribute value greater than zero ("required any"), prevents InfoPath from deterministically creating a valid instance for this schema fragment.</span></span> <span data-ttu-id="1ec9a-124">InfoPath deve ser capaz de criar uma instância válida ao gerar um formulário que usa esse fragmento de esquema.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-124">InfoPath must be able to create a valid instance when generating a form that uses this schema fragment.</span></span> <span data-ttu-id="1ec9a-125">Como parte da execução do **Assistente de fonte de dados**, esquemas com necessárias **xsd: qualquer** elementos exigem que você escolher qual elemento de esquema que você deseja usar no lugar required **xsd: qualquer** elemento.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-125">As part of running the **Data Source Wizard**, schemas with required **xsd:any** elements require you to choose which schema element you want to use in place of the required **xsd:any** element.</span></span> 
  
## <a name="elements-with-an-abstract-complex-type"></a><span data-ttu-id="1ec9a-126">Elementos com um tipo complexo abstrato</span><span class="sxs-lookup"><span data-stu-id="1ec9a-126">Elements with an Abstract Complex Type</span></span>

<span data-ttu-id="1ec9a-127">Modo de design do InfoPath oferece suporte a criação de um modelo de formulário com base em esquemas que usam tipos complexos abstratos.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-127">InfoPath design mode supports designing a form template against schemas that use abstract complex types.</span></span> <span data-ttu-id="1ec9a-128">Por exemplo, se um elemento chamado `shippingAddress` tem um tipo complexo abstrato denominado `address` que tem duas derivações, `USAddress` e `CanadianAddress`, InfoPath trata qualquer instância de `shippingAddress` como uma opção entre `shippingAddress` com tipo `USAddress` e `shippingAddress` com tipo `CanadianAddress` .</span><span class="sxs-lookup"><span data-stu-id="1ec9a-128">For example, if an element named  `shippingAddress` has an abstract complex type named  `address` that has two derivations,  `USAddress` and  `CanadianAddress`, InfoPath treats any instance of  `shippingAddress` as a choice between  `shippingAddress` with type  `USAddress` and  `shippingAddress` with type  `CanadianAddress` .</span></span> <span data-ttu-id="1ec9a-129">Neste exemplo, se os esquemas fornecidos não contenham nenhum tipos que derivam do endereço, em seguida, InfoPath solicitações de um esquema adicional que atende a esse requisito.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-129">In this example, if the provided schemas contain no types that derive from address, then InfoPath requests an additional schema that fulfills this requirement.</span></span> 
  
## <a name="xsd-constructs-with-reduced-functionality"></a><span data-ttu-id="1ec9a-130">Construções XSD com funcionalidade reduzida</span><span class="sxs-lookup"><span data-stu-id="1ec9a-130">XSD Constructs with Reduced Functionality</span></span>

<span data-ttu-id="1ec9a-131">As seções a seguir descrevem construções XSD que reduziram funcionalidade quando usado para criar um modelo de formulário no designer de formulários do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-131">The following sections describe XSD constructs that have reduced functionality when used to create a form template in the InfoPath form designer.</span></span>
  
## <a name="substitution-groups"></a><span data-ttu-id="1ec9a-132">Grupos de substituição</span><span class="sxs-lookup"><span data-stu-id="1ec9a-132">Substitution Groups</span></span>

<span data-ttu-id="1ec9a-133">Todos os membros do grupo de substituição aparecem no painel de tarefas **campos** .</span><span class="sxs-lookup"><span data-stu-id="1ec9a-133">All members of the substitution group appear in the **Fields** task pane.</span></span> <span data-ttu-id="1ec9a-134">InfoPath representa as possibilidades de substituição como uma opção de todos os grupos de substituição (incluindo o elemento determinantes, se não for abstrata).</span><span class="sxs-lookup"><span data-stu-id="1ec9a-134">InfoPath represents the substitution possibilities as a choice of all the substitution groups (including the defining element, if it is not abstract).</span></span> <span data-ttu-id="1ec9a-135">Se não houver nenhuma grupos de substituição para um elemento abstrato, InfoPath solicita que você forneça um esquema que contém pelo menos um elemento que é um grupo de substituição.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-135">If there are no substitution groups for an abstract element, InfoPath prompts you to provide a schema that contains at least one element that is a substitution group.</span></span> 
  
## <a name="unbounded-choice-elements"></a><span data-ttu-id="1ec9a-136">Elementos de opção não vinculados</span><span class="sxs-lookup"><span data-stu-id="1ec9a-136">Unbounded Choice Elements</span></span>

<span data-ttu-id="1ec9a-137">O fragmento de esquema a seguir mostra um elemento de escolha não vinculado:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-137">The following schema fragment shows an unbounded choice element:</span></span>
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

<span data-ttu-id="1ec9a-138">InfoPath exibe os elementos de escolha de repetição como escolhas no painel de tarefas de **campos** de repetição.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-138">InfoPath displays repeating choice elements as repeating choices in the **Fields** task pane.</span></span> <span data-ttu-id="1ec9a-139">Não há um controle de **Grupo de escolha de repetição** que você pode usar para representar a lista heterogênea definida pelo elemento de escolha de repetição em XSD.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-139">There is a **Repeating Choice Group** control that you can use to represent the heterogeneous list defined by the repeating choice element in the XSD.</span></span> 
  
## <a name="repeating-sequence"></a><span data-ttu-id="1ec9a-140">Sequência de repetição</span><span class="sxs-lookup"><span data-stu-id="1ec9a-140">Repeating Sequence</span></span>

<span data-ttu-id="1ec9a-141">O fragmento de esquema a seguir mostra uma sequência de repetição:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-141">The following schema fragment shows a repeating sequence:</span></span>
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

<span data-ttu-id="1ec9a-142">Desde que a repetição sequência contiver um elemento necessário, o InfoPath carrega a XSD sem modificá-lo e permite associar controles de seção de repetição à sequência de repetição.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-142">As long as the repeating sequence contains a required element, InfoPath loads the XSD without modifying it and allows you to bind repeating section controls to the repeating sequence.</span></span>
  
## <a name="choice-of-model-groups"></a><span data-ttu-id="1ec9a-143">Escolha dos grupos de modelo</span><span class="sxs-lookup"><span data-stu-id="1ec9a-143">Choice of Model Groups</span></span>

<span data-ttu-id="1ec9a-144">O fragmento de esquema a seguir mostra o elemento de opção que contém vários grupos de modelo:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-144">The following schema fragment shows the choice element containing several model groups:</span></span>
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

<span data-ttu-id="1ec9a-145">Modo de design do InfoPath oferece suporte a tais construções XSD sem exigir qualquer modificação pelo criador do formulário.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-145">InfoPath design mode supports such XSD constructs without requiring any modification by the form designer.</span></span> <span data-ttu-id="1ec9a-146">Enquanto o InfoPath não modifica o significado do esquema, ele simplifica a construção de opção acima em uma única opção no painel de tarefas **campos** do recolhido equivalente.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-146">While InfoPath does not modify the meaning of the schema, it simplifies the choice construct above into an equivalent collapsed single choice in the **Fields** task pane.</span></span> 
  
## <a name="optional-sibling-with-same-qualified-name"></a><span data-ttu-id="1ec9a-147">Irmão opcional com mesmo nome qualificado</span><span class="sxs-lookup"><span data-stu-id="1ec9a-147">Optional Sibling with Same Qualified Name</span></span>

<span data-ttu-id="1ec9a-148">O fragmento de esquema a seguir mostra um irmão opcional com mesmo nome qualificado (`QName`):</span><span class="sxs-lookup"><span data-stu-id="1ec9a-148">The following schema fragment shows an optional sibling with same qualified name (`QName`):</span></span>
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

<span data-ttu-id="1ec9a-149">As expressões **XPath** para esses nós podem ser complexas, porque cada instância XML possível deve ser contabilizada no designer de formulários do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-149">**XPath** expressions for these nodes can be complex because every potential XML instance must be accounted for in the InfoPath form designer.</span></span> <span data-ttu-id="1ec9a-150">InfoPath não expõe partes do esquema para o qual talvez tenha dificuldade para criar associações de **XPath** corretas.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-150">InfoPath does not expose parts of the schema for which it may have difficulty creating correct **XPath** bindings.</span></span> <span data-ttu-id="1ec9a-151">Avisos aparecem sobre as partes do esquema que serão ignoradas.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-151">Warnings appear regarding the portions of the schema that are ignored.</span></span> 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a><span data-ttu-id="1ec9a-152">Construções XSD com significado especial no InfoPath</span><span class="sxs-lookup"><span data-stu-id="1ec9a-152">XSD Constructs with Special Meaning in InfoPath</span></span>

<span data-ttu-id="1ec9a-153">As seções a seguir descrevem construções XSD que têm um significado especial quando usado na criação de um modelo de formulário no modo de design.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-153">The following sections describe XSD constructs that have special meaning when used in creating a form template in design mode.</span></span> <span data-ttu-id="1ec9a-154">Estas seções descrevem como você pode usar as construções no seu esquema para habilitar determinados comportamentos.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-154">These sections describe how you can use the constructs in your schema to enable certain behaviors.</span></span>
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a><span data-ttu-id="1ec9a-155">Adicionando novos campos de elemento e grupos com o painel de tarefas de campos</span><span class="sxs-lookup"><span data-stu-id="1ec9a-155">Adding New Element Fields and Groups with the Fields Task Pane</span></span>

<span data-ttu-id="1ec9a-156">Você pode construir o esquema para que você possa usar o painel de tarefas **campos** para adicionar novos campos de elemento e grupos a um elemento em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-156">You can construct your schema so that you can use the **Fields** task pane to add new element fields and groups to an element at design time.</span></span> <span data-ttu-id="1ec9a-157">Para fazer isso, você declarar um elemento no seu esquema com um opcional, não acoplados **xsd: qualquer** elemento que especifica o atributo de namespace com o **# # any** curinga.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-157">To do so, you declare an element in your schema with an optional, unbounded **xsd:any** element that specifies the namespace attribute with the **##any** wildcard.</span></span> <span data-ttu-id="1ec9a-158">Em seguida, no modo de design, você pode usar o painel de tarefas **campos** para adicionar novos campos de elemento e grupos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-158">Then, in design mode, you can use the **Fields** task pane to add new element fields and groups to that element.</span></span> <span data-ttu-id="1ec9a-159">Por exemplo, você pode adicionar novo conteúdo para o elemento a seguir:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-159">For example, you could add new content to the following element:</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a><span data-ttu-id="1ec9a-160">Adicionando novos campos de atributo com os campos de painel de tarefas</span><span class="sxs-lookup"><span data-stu-id="1ec9a-160">Adding New Attribute Fields with the Fields Task Pane</span></span>

<span data-ttu-id="1ec9a-161">Da mesma forma como no caso de elemento, você pode declarar um atributo com um elemento **anyAttribute** que tem o atributo do namespace especificado como o **# # any** curinga.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-161">Similarly to the element case, you can declare an attribute with an **anyAttribute** element that has the namespace attribute specified as the **##any** wildcard.</span></span> <span data-ttu-id="1ec9a-162">Em tempo de design, você pode usar o painel de tarefas **campos** para adicionar novo conteúdo para que esse atributo de esquema.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-162">At design time, you can use the **Fields** task pane to add new content to that schema attribute.</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a><span data-ttu-id="1ec9a-163">Armazenando assinaturas XML na fonte de dados</span><span class="sxs-lookup"><span data-stu-id="1ec9a-163">Storing XML Signatures in the Data Source</span></span>

<span data-ttu-id="1ec9a-164">Para habilitar usuários assinar digitalmente um formulário em tempo de execução, o esquema da fonte de dados deve declarar um elemento chamado assinatura para armazenar as informações de assinaturas de XML (assinatura digital) que são criadas quando um usuário se conecta o formulário.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-164">To enable users to digitally sign a form at run time, the schema of the data source must declare an element named signature for storing the XML Signatures (digital signature) information that is created when a user signs the form.</span></span> <span data-ttu-id="1ec9a-165">Você tornar esta declaração usando o **xsd: qualquer** elemento com o atributo do namespace especificado como o namespace de assinaturas XML com um caractere curinga, da seguinte maneira: "http://www.w3c.org/2000/09/xmldsig#"</span><span class="sxs-lookup"><span data-stu-id="1ec9a-165">You make this declaration by using the **xsd:any** element with the namespace attribute specified as the XML Signatures namespace with a wildcard character, as follows: "http://www.w3c.org/2000/09/xmldsig#"</span></span> 
  
```XML
<xsd:element name="signature"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3c.org/2000/09/xmldsig#"  
             processContents="lax" minOccurs="0" maxOccurs="unbounded"/> 
        <xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="binding-a-field-to-a-rich-text-box-control"></a><span data-ttu-id="1ec9a-166">Associando um campo a um controle de caixa de Rich Text</span><span class="sxs-lookup"><span data-stu-id="1ec9a-166">Binding a Field to a Rich Text Box Control</span></span>

 <span data-ttu-id="1ec9a-167">Controles de **Caixa de Rich Text** no InfoPath gerarem genérico XHTML; Consequentemente, seu esquema deve especificar que qualquer número de texto e nós XHTML é válido no XML da instância do formulário.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-167">**Rich Text Box** controls in InfoPath generate generic XHTML; consequently, your schema must specify that any number of text and XHTML nodes is valid in the XML of the form instance.</span></span> <span data-ttu-id="1ec9a-168">É possível conseguir essa especificação com a construção XSD a seguir:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-168">You can achieve this specification with the following XSD construct:</span></span> 
  
```XML
<xsd:element name="xhtml"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="http://www.w3.org/1999/xhtml" processContents="lax"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

> [!NOTE]
> <span data-ttu-id="1ec9a-169">InfoPath nunca modifica o conteúdo do arquivo do esquema (. xsd), mas ela pode interpretar logicamente um subconjunto dela para fins de design.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-169">InfoPath never modifies the content of the schema file (.xsd), but it may logically infer a subset of it for design purposes.</span></span> <span data-ttu-id="1ec9a-170">O arquivo de esquema é sempre tocado dentro do modelo de formulário em tempo de design e tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-170">The schema file is always untouched within the form template at both design time and run time.</span></span> 
  
## <a name="debugging-common-xsd-errors"></a><span data-ttu-id="1ec9a-171">Depuração de erros comuns de XSD</span><span class="sxs-lookup"><span data-stu-id="1ec9a-171">Debugging Common XSD Errors</span></span>

<span data-ttu-id="1ec9a-172">Se você carregar arquivos XSD externamente criados para criar modelos de formulário no designer de formulários do InfoPath, você pode receber um dos dois tipos de mensagens de erro: MSXML mensagens de erro ou mensagens de erro do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-172">If you load externally authored XSD files to create form templates in the InfoPath form designer, you may receive either of two types of error messages: MSXML error messages or InfoPath error messages.</span></span> <span data-ttu-id="1ec9a-173">Mensagens de erro do MSXML aparecem na seção de **detalhes** de uma caixa de diálogo de mensagem de erro do InfoPath, e eles sempre comecem com uma referência para o nome ou o caminho do arquivo de esquema que está gerando o erro.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-173">MSXML error messages appear in the **Details** section of an InfoPath error message dialog box, and they always begin with a reference to the name or path of the schema file that is raising the error.</span></span> <span data-ttu-id="1ec9a-174">Algumas construções de esquema XSD válidas não são suportadas pelo InfoPath; Estas são abordadas na seção constrói de XSD sem suporte.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-174">Some valid XSD schema constructs are not supported by InfoPath; these are discussed in the Unsupported XSD Constructs section.</span></span> <span data-ttu-id="1ec9a-175">As seções a seguir descrevem alguns erros comuns que podem causar esquemas Falha ao carregar com êxito no InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-175">The following sections describe some common errors that can cause schemas to fail to load successfully in InfoPath.</span></span> 
  
## <a name="the-xsd-namespace-declaration"></a><span data-ttu-id="1ec9a-176">A declaração de Namespace XSD</span><span class="sxs-lookup"><span data-stu-id="1ec9a-176">The XSD Namespace Declaration</span></span>

<span data-ttu-id="1ec9a-177">Semelhante ao todos os padrões W3C, esquemas XML (XSD) passou por um processo de revisão longos em seu caminho para se tornar uma recomendação.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-177">Similar to all W3C standards, XML Schemas (XSD) went through a lengthy review process on its way to becoming a recommendation.</span></span> <span data-ttu-id="1ec9a-178">Havia muitas rascunhos de trabalho e, consequentemente, muitos arquivos XSD foram gravados com base nos seguintes evoluindo padrões.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-178">There were many working drafts, and consequently, many XSD files were written based on these evolving standards.</span></span> <span data-ttu-id="1ec9a-179">Durante esse processo, a Microsoft criou uma linguagem de esquema proprietárias chamada XML-Data Reduced (XDR) que foi incluído no MSXML 3.0.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-179">During this process, Microsoft created a proprietary schema language called XML-Data Reduced (XDR) that was included with MSXML 3.0.</span></span> <span data-ttu-id="1ec9a-180">Começando com a versão do MSXML 4.0, o Microsoft XML Core Services oferece suporte a recomendação completa da XSD.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-180">Starting with the release of MSXML 4.0, Microsoft XML Core Services supports the full recommendation of XSD.</span></span> <span data-ttu-id="1ec9a-181">Muitos programas para a criação de esquemas não aguardou XSD para se tornar uma recomendação completa.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-181">Many programs for creating schemas did not wait for XSD to become a full recommendation.</span></span> <span data-ttu-id="1ec9a-182">Versões mais antigas desses programas podem produzir arquivos XSD desatualizados que a infra-estrutura do MSXML 5.0, do qual o InfoPath depende, não oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-182">Older versions of these programs may produce outdated XSD files that the MSXML 5.0 infrastructure, on which InfoPath depends, does not support.</span></span>
  
<span data-ttu-id="1ec9a-183">Para garantir que um arquivo XSD suporta a recomendação de XSD completa, ele deve conter a seguinte declaração de namespace XML no \<esquema\> tag:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-183">To ensure that an XSD file supports the full XSD recommendation, it should contain the following XML namespace declaration in the \<schema\> tag:</span></span>
  
```XML
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
```

<span data-ttu-id="1ec9a-184">Da mesma forma que todas as declarações de namespace XML, o prefixo XML (no caso 'xsd') pode ser qualquer cadeia de caracteres de prefixo válido.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-184">Similar to all XML namespace declarations, the XML prefix (in this case 'xsd') can be any valid prefix string.</span></span> <span data-ttu-id="1ec9a-185">Alguns prefixos comuns, talvez você veja prática são 'xsd', 'x,' e ' (sem prefixo).</span><span class="sxs-lookup"><span data-stu-id="1ec9a-185">Some common prefixes you may see in practice are 'xsd', 'xs', and '' (no prefix).</span></span> <span data-ttu-id="1ec9a-186">MSXML geralmente relata um erro sobre a raiz não está sendo definida corretamente se esta declaração de namespace está ausente.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-186">MSXML usually reports an error about the root not being properly defined if this namespace declaration is missing.</span></span>
  
## <a name="importing-and-including-schemas"></a><span data-ttu-id="1ec9a-187">Importando e incluindo esquemas</span><span class="sxs-lookup"><span data-stu-id="1ec9a-187">Importing and Including Schemas</span></span>

<span data-ttu-id="1ec9a-188">Esquemas XSD são extensíveis e importe e incluir outros esquemas.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-188">XSD schemas are extensible and can import and include other schemas.</span></span> <span data-ttu-id="1ec9a-189">Em geral, você deve importar um esquema se o esquema especificado no atributo **targetNamespace** difere do esquema atual.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-189">Generally, you should import a schema if the schema specified in the **targetNamespace** attribute differs from the current schema.</span></span> <span data-ttu-id="1ec9a-190">Você deve incluí-lo se o esquema especificado no atributo **targetNamespace** é o mesmo que o esquema atual.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-190">You should include it if the schema specified in the **targetNamespace** attribute is the same as the current schema.</span></span> 
  
<span data-ttu-id="1ec9a-191">A semântica de importação e incluindo esquemas é:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-191">The semantics for importing and including schemas are as follows:</span></span>
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

<span data-ttu-id="1ec9a-192">Se o atributo **schemaLocation** estiver faltando (como acontece com alguns conversores), e depois MSXML gerará um erro, porque não é possível encontrar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-192">If the **schemaLocation** attribute is missing (as happens with some converters), then MSXML raises an error because it cannot find the file.</span></span> <span data-ttu-id="1ec9a-193">Se você receber esse erro, também Certifique-se de que o recurso ou o local especificado no atributo schemaLocation está acessível pelos usuários do modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-193">If you get this error, also check to make sure that the resource or location specified in the schemaLocation attribute is accessible by users of the form template.</span></span> <span data-ttu-id="1ec9a-194">Obviamente, erros ocorrem se o atributo **schemaLocation** faz referência a um servidor ou o diretório que está inoperante ou inexistente, ou se os usuários não têm permissões de acesso.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-194">Obviously, errors occur if the **schemaLocation** attribute references a server or directory that is down or nonexistent or if users do not have access permissions.</span></span> <span data-ttu-id="1ec9a-195">Além disso, certifique-se de examinar todos os esquemas importados e incluídos para certificar-se de que eles são válidos.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-195">Also, be sure to examine all imported and included schemas to make sure they are valid.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1ec9a-196">Erros causados por problemas com o atributo **schemaLocation** são um problema quando o InfoPath primeiro importa os esquemas; ou seja, quando você inicia a criação de um formulário baseado em um esquema existente.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-196">Errors caused by problems with the **schemaLocation** attribute are an issue only when InfoPath first imports the schemas; that is, when you first start designing a form based on an existing schema.</span></span> <span data-ttu-id="1ec9a-197">Depois disso, o InfoPath funciona com versões em cache dos arquivos de esquema que são armazenados no modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-197">After that, InfoPath works with cached versions of the schema files that are stored in the form template.</span></span> 
  
<span data-ttu-id="1ec9a-198">Um atributo de namespace vazio é permitido durante a importação de um esquema, se esse esquema não especificar um atributo **targetNamespace** .</span><span class="sxs-lookup"><span data-stu-id="1ec9a-198">An empty namespace attribute is allowed when importing a schema, if that schema does not specify a **targetNamespace** attribute.</span></span> <span data-ttu-id="1ec9a-199">Em geral, o espaço para nome na página Importar deve corresponder o **targetNamespace** especificado no esquema de que você importar.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-199">In general, the namespace on the import must match the **targetNamespace** specified in the schema that you import.</span></span> 
  
## <a name="nondeterministic-schemas"></a><span data-ttu-id="1ec9a-200">Esquemas não determinísticas</span><span class="sxs-lookup"><span data-stu-id="1ec9a-200">Nondeterministic Schemas</span></span>

<span data-ttu-id="1ec9a-201">A infraestrutura de MSXML 5.0 que depende do InfoPath confiável pode detectar e geram erros para alertá-lo aos esquemas não determinísticas, mas a mensagem de erro resultante não fornece um número de linha para dizer que parte do esquema é elevar o erro.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-201">The MSXML 5.0 infrastructure that InfoPath depends upon can reliably detect and raise errors to alert you to nondeterministic schemas, but the resultant error message does not provide a line number to tell you which part of the schema is raising the error.</span></span> <span data-ttu-id="1ec9a-202">Esta seção discute porque é importante para os arquivos de esquema XSD ser determinantes e o que significa ser não determinístico.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-202">This section discusses why it is important for XSD schema files to be deterministic and what it means to be nondeterministic.</span></span> <span data-ttu-id="1ec9a-203">Ele também mostra alguns erros comuns para evitar.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-203">It also shows some common errors to avoid.</span></span>
  
<span data-ttu-id="1ec9a-204">Esquemas XSD existirem com o objetivo de validar semântica de estrutura e o tipo de dados XML.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-204">XSD schemas exist for the purpose of validating XML data structure and type semantics.</span></span> <span data-ttu-id="1ec9a-205">Para realizar essa tarefa, o sistema de validação (no caso, MSXML 5.0) deve mapear nós XML para declarações de XSD.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-205">To accomplish this task, the validating system (in this case, MSXML 5.0) must map XML nodes to XSD declarations.</span></span> <span data-ttu-id="1ec9a-206">Sem esse mapeamento, o sistema de validação não é possível realizar suas tarefas.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-206">Without this mapping, the validating system cannot accomplish its task.</span></span> <span data-ttu-id="1ec9a-207">Se um mapeamento pode ser garantido, o esquema é determinante.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-207">If a mapping can be guaranteed, then the schema is deterministic.</span></span> <span data-ttu-id="1ec9a-208">Se houver uma única instância XML que torna impossível esse mapeamento, o esquema é não determinístico.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-208">If there is a single XML instance that makes this mapping impossible, then the schema is nondeterministic.</span></span>
  
<span data-ttu-id="1ec9a-209">O esquema de exemplo a seguir é não determinístico:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-209">The following example schema is nondeterministic:</span></span>
  
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

<span data-ttu-id="1ec9a-210">Para ilustrar o motivo pelo qual este segmento XSD é não determinístico, pressupõem que você tem o seguinte fragmento XML que você deseja validar com esse esquema:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-210">To illustrate why this XSD segment is nondeterministic, assume you have the following XML fragment that you want to validate with this schema:</span></span>
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

<span data-ttu-id="1ec9a-211">Neste fragmento de XML, não é criptografado se o * \<file_path\> * elemento é o nó obrigatório da primeira parte da declaração de opção ou uma opcional da segunda parte da declaração de opção.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-211">In this XML fragment, it is not clear whether the  *\<file_path\>*  element is the required node from the first part of the choice declaration or the optional one from the second part of the choice declaration.</span></span> <span data-ttu-id="1ec9a-212">Essa distinção é importante pelos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-212">This distinction is important for the following reasons:</span></span> 
  
1. <span data-ttu-id="1ec9a-213">Se o fragmento XML é validado em relação a primeira parte da declaração de opção, o XML é válido em relação ao esquema.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-213">If the XML fragment is validated against the first part of the choice declaration, then the XML is valid against the schema.</span></span>
    
2. <span data-ttu-id="1ec9a-214">Se o fragmento XML é validado em relação a segunda parte da declaração de opção, então o esquema não é válido, pois required \<URI\> nó está ausente.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-214">If the XML fragment is validated against the second part of the choice declaration, then the schema is not valid, because the required \<URI\> node is missing.</span></span> 
    
<span data-ttu-id="1ec9a-215">Alguns sistemas de validação XSD err em direção Validando contra este esquema porque não há um caminho válido.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-215">Some XSD validation systems err toward validating against this schema because there is a valid path.</span></span> <span data-ttu-id="1ec9a-216">MSXML é mais restrito e gera um erro informando que o esquema é não determinístico.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-216">MSXML is stricter and raises an error stating that the schema is nondeterministic.</span></span>
  
<span data-ttu-id="1ec9a-217">O que segue é alguns exemplos de mais de esquemas não determinísticas.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-217">What follows are a few more examples of nondeterministic schemas.</span></span> <span data-ttu-id="1ec9a-218">O primeiro lida com elementos opcionais.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-218">The first deals with optional elements.</span></span> <span data-ttu-id="1ec9a-219">Nesses casos frequentemente provenientes de XDR conversores XSD devido às diferenças na cardinalities padrão nos idiomas dois esquema.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-219">These cases often arise from XDR to XSD converters because of differences in the default cardinalities in the two schema languages.</span></span> <span data-ttu-id="1ec9a-220">O primeiro caso a serem considerados é opcionais elementos declarados com elementos **xsd:choice** e **xsd:sequence** .</span><span class="sxs-lookup"><span data-stu-id="1ec9a-220">The first case to consider is optional elements declared with **xsd:choice** and **xsd:sequence** elements.</span></span> <span data-ttu-id="1ec9a-221">Elementos opcionais declarados em um elemento **xsd:sequence** geralmente validar corretamente, desde que você não possui elementos com o mesmo nome mais de uma vez, com apenas os elementos opcionais entre si.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-221">Optional elements declared in an **xsd:sequence** element usually validate properly, as long as you do not have elements with the same name more than once, with only optional elements in between.</span></span> <span data-ttu-id="1ec9a-222">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-222">For example:</span></span> 
  
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

<span data-ttu-id="1ec9a-223">Para entender por que esse segmento do esquema é não determinístico, pressupõem que você tem o inválido fragmento XML a seguir:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-223">To understand why this schema segment is nondeterministic, assume you have the following invalid XML fragment:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
    <anotherNode/> 
</container> 

```

<span data-ttu-id="1ec9a-224">Olhando esse fragmento, você pode ver por que ele é inválido: há dois `<aNode>` elementos antes do `<anotherNode>` elemento, quando somente um é permitido.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-224">Looking at this fragment, you can see why it is invalid: there are two  `<aNode>` elements before the  `<anotherNode>` element, when only one is allowed.</span></span> 
  
<span data-ttu-id="1ec9a-225">Agora, suponha que você tenha a seguinte instância XML para validar:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-225">Now assume that you have the following XML instance to validate:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

<span data-ttu-id="1ec9a-226">O desafio é para determinar se esta instância é válida.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-226">The challenge is to determine whether this instance is valid.</span></span> <span data-ttu-id="1ec9a-227">Você tem dois `<aNode>` elementos onde somente um é permitido ou tem um `<aNode>` elemento onde ele é permitido e outro onde é permitido?</span><span class="sxs-lookup"><span data-stu-id="1ec9a-227">Do you have two  `<aNode>` elements where only one is allowed, or do you have an  `<aNode>` element where it is allowed and another where it is allowed?</span></span> <span data-ttu-id="1ec9a-228">O esquema é não determinístico porque não é possível saber.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-228">The schema is nondeterministic because there is no way to know.</span></span> 
  
<span data-ttu-id="1ec9a-229">Da mesma forma, os elementos opcionais declarados em um elemento **xsd:choice** são geralmente problemáticos.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-229">Similarly, optional elements declared in an **xsd:choice** element are usually problematic.</span></span> <span data-ttu-id="1ec9a-230">No exemplo a seguir simplificado, há um meio para determinar se a opção ocorreu depois com o elemento opcional não estar ao vivo ou se ele nunca ocorreu nisso.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-230">In the following simplified example, there is no way to determine whether the choice occurred once with the optional element not being there or whether it never occurred at all.</span></span> 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

<span data-ttu-id="1ec9a-231">A prática questionável final está usando um **xsd: qualquer** elemento sem uma definição de namespace, como em `<xsd:any namespace="##other"/>` , após um elemento **xsd:sequence** .</span><span class="sxs-lookup"><span data-stu-id="1ec9a-231">The final questionable practice is using an **xsd:any** element without a namespace definition, as in  `<xsd:any namespace="##other"/>` , after an **xsd:sequence** element.</span></span> <span data-ttu-id="1ec9a-232">Essa construção é especialmente problemática quando vier um elemento opcional.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-232">This construct is especially troublesome when it follows an optional element.</span></span> <span data-ttu-id="1ec9a-233">Se você rever o exemplo anterior e altera o último nó para um **xsd: qualquer** elemento, você pode ver que todos os argumentos anteriores sobre nondeterminism ainda se aplicam, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-233">If you revisit the previous example and change just the last node to an **xsd:any** element, you can see that all the previous arguments about nondeterminism still apply, as follows:</span></span> 
  
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

## <a name="illegal-enumeration-values"></a><span data-ttu-id="1ec9a-234">Valores de enumeração ilegais</span><span class="sxs-lookup"><span data-stu-id="1ec9a-234">Illegal Enumeration Values</span></span>

<span data-ttu-id="1ec9a-235">Esquemas XSD geralmente não realize qualquer tipo de validação até que você valida um documento de instância real.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-235">XSD schemas typically do not perform any type validation until you validate an actual instance document.</span></span> <span data-ttu-id="1ec9a-236">Uma exceção é quando você tem uma enumeração no seu esquema.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-236">An exception to this is when you have an enumeration in your schema.</span></span> <span data-ttu-id="1ec9a-237">Nesse caso, o esquema valida os valores de enumeração contra os tipos de enumeração para garantir que eles são valores de nó apropriado.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-237">In this case, the schema validates the enumeration values against the enumeration types to ensure they are proper node values.</span></span> <span data-ttu-id="1ec9a-238">Aqui estão dois exemplos:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-238">Here are two examples:</span></span>
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="1ec9a-239">Este esquema é inválido, como "11 horas" não é um valor válido para um elemento do tipo **xsd: time**.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-239">This schema is invalid because "eleven o'clock" is not a valid value for an element of type **xsd:time**.</span></span>
  
<span data-ttu-id="1ec9a-240">Este é um exemplo mais complexo:</span><span class="sxs-lookup"><span data-stu-id="1ec9a-240">The following is a more complex example:</span></span>
  
```XML
<xsd:simpleType name="concession"> 
    <xsd:restriction base="xsd:NMTOKEN"> 
        <xsd:enumeration value="GummyBears"/> 
        <xsd:enumeration value="SnowCaps"/> 
        <xsd:enumeration value="M&Ms"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="1ec9a-241">Para entender por que neste exemplo é inválido, é preciso entender como o tipo **xsd:NMTOKEN** é definido.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-241">To understand why this example is invalid, you must understand how the type **xsd:NMTOKEN** is defined.</span></span> <span data-ttu-id="1ec9a-242">A especificação de tipos de dados W3C define o tipo **NMTOKEN** da seguinte maneira: "É qualquer mistura de caracteres de nome de um NMTOKEN (token nome)."</span><span class="sxs-lookup"><span data-stu-id="1ec9a-242">The W3C data types specification defines the **NMTOKEN** type as follows: "An NMTOKEN (name token) is any mixture of name characters."</span></span> 
  
<span data-ttu-id="1ec9a-243">Se você investigar melhor, você descobre que ' e ' não é um nome válido de caractere e, portanto, "M & Ms" não valida como um tipo **NMTOKEN** .</span><span class="sxs-lookup"><span data-stu-id="1ec9a-243">If you investigate further, you find that '&' is not a valid name character, and therefore "M&Ms" does not validate as an **NMTOKEN** type.</span></span> 
  
## <a name="empty-sequence-or-choice-elements"></a><span data-ttu-id="1ec9a-244">Sequência vazia ou elementos de opção</span><span class="sxs-lookup"><span data-stu-id="1ec9a-244">Empty Sequence or Choice Elements</span></span>

<span data-ttu-id="1ec9a-245">Às vezes, o MSXML gera erros sobre declarações de esquema que contêm vazio **xsd:choice** ou **xsd:sequence** elementos, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-245">MSXML sometimes raises errors about schema declarations that contain empty **xsd:choice** or **xsd:sequence** elements, as shown in the following example.</span></span> 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="1ec9a-246">Removendo a esvaziar `<xsd:choice />` marca deve resolver esse problema.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-246">Removing the empty  `<xsd:choice />` tag should resolve this problem.</span></span> 
  
## <a name="regular-expressions"></a><span data-ttu-id="1ec9a-247">Expressões Regulares</span><span class="sxs-lookup"><span data-stu-id="1ec9a-247">Regular Expressions</span></span>

<span data-ttu-id="1ec9a-248">MSXML 5.0 pode ter problemas ao validar os padrões de expressão regular no carregamento.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-248">MSXML 5.0 can have problems validating regular expression patterns on load.</span></span> <span data-ttu-id="1ec9a-249">Expressões regulares podem ser complexas, e você deve tomar cuidado quando você estiver usando-los.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-249">Regular expressions can be complicated, and you should be careful when you are using them.</span></span> <span data-ttu-id="1ec9a-250">Cada analisador XSD parece ter idiomas de expressão regular flexível; ou seja, implemente a linguagem de expressão regular XSD oficial mais elementos de outros idiomas de expressão regular.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-250">Every XSD parser seems to have flexible regular expression languages; that is, they implement the official XSD regular expression language plus elements from other regular expression languages.</span></span> <span data-ttu-id="1ec9a-251">Se o designer de formulários do InfoPath tiver problemas ao analisar uma expressão regular, os dados de amostra que InfoPath gera seja inválidos ou não podem ser gerados em todos os.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-251">If InfoPath form designer has problems parsing a regular expression, then the sample data InfoPath generates might be invalid or might not be generated at all.</span></span> <span data-ttu-id="1ec9a-252">Isso é aceitável em tempo de design, porque o InfoPath usa apenas os dados de amostra para formatação.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-252">This is acceptable at design time, because InfoPath uses only sample data for formatting.</span></span> <span data-ttu-id="1ec9a-253">No entanto, se você usar uma expressão regular que não oferece suporte a MSXML, InfoPath não é possível validar um valor em relação a ele quando um usuário preenche um formulário.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-253">However, if you use a regular expression that MSXML does not support, then InfoPath cannot validate a value against it when a user is filling out a form.</span></span> <span data-ttu-id="1ec9a-254">[Parte do esquema XML 0: Primer Second Edition](http://www.w3.org/TR/xmlschema-0/)descreve o que é suportado em expressões regulares de XSD.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-254">[XML Schema Part 0: Primer Second Edition](http://www.w3.org/TR/xmlschema-0/)describes what is supported in XSD regular expressions.</span></span> <span data-ttu-id="1ec9a-255">Para obter mais informações sobre expressões regulares de XSD e expressões regulares de nível 1 de Unicode, consulte [Expressões regulares Unicode](http://www.unicode.org/reports/tr18/) .</span><span class="sxs-lookup"><span data-stu-id="1ec9a-255">For more information about XSD regular expressions and Unicode level 1 regular expressions, see [Unicode Regular Expressions](http://www.unicode.org/reports/tr18/) .</span></span> 
  
## <a name="targetnamespace-attribute-issues"></a><span data-ttu-id="1ec9a-256">targetNamespace problemas de atributo</span><span class="sxs-lookup"><span data-stu-id="1ec9a-256">targetNamespace Attribute Issues</span></span>

<span data-ttu-id="1ec9a-257">XSD é interessante em que, por padrão, o atributo **targetNamespace** refere-se ao somente as declarações de nível superior, embora você possa definir `attributeFormDefault=qualified` e `elementFormDefault=qualified` para substituir esse comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-257">XSD is interesting in that, by default, the **targetNamespace** attribute refers to only the top-level declarations, although you can set  `attributeFormDefault=qualified` and  `elementFormDefault=qualified` to override this default behavior.</span></span> <span data-ttu-id="1ec9a-258">Como exemplo, suponha que você tenha a seguir XSD.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-258">As an example, assume that you have the following XSD.</span></span> 
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element name="local"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
</xsd:schema> 

```

<span data-ttu-id="1ec9a-259">E que, seu XML instância documento semelhante ao exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-259">And that, your XML instance document resembles the following example.</span></span>
  
```XML
<ns:root xmlns:ns="http://ns"> 
    <local/> 
</ns:root> 

```

<span data-ttu-id="1ec9a-260">Definições de locais não exigem o namespace de destino porque qualificação está desativada por padrão.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-260">Local definitions do not require the target namespace because qualification is turned off by default.</span></span> <span data-ttu-id="1ec9a-261">No entanto, se você alterar sua definição de local para ser global, sua referência deve ser qualificada com o prefixo do namespace.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-261">However, if you change your local definition to be global, then your reference must be qualified with the namespace prefix.</span></span> <span data-ttu-id="1ec9a-262">Por exemplo, o esquema a seguir é inválido.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-262">For example, the following schema is invalid.</span></span>
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" targetNamespace="http://ns" > 
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

<span data-ttu-id="1ec9a-263">Este esquema é inválido porque é "global" no namespace "http://ns".</span><span class="sxs-lookup"><span data-stu-id="1ec9a-263">This schema is invalid because "global" is in the namespace "http://ns".</span></span> <span data-ttu-id="1ec9a-264">O simple ref = "global" não seja reconhecida porque o namespace padrão não é "http://ns".</span><span class="sxs-lookup"><span data-stu-id="1ec9a-264">The simple ref="global" is not recognized because the default namespace is not "http://ns".</span></span> <span data-ttu-id="1ec9a-265">Para corrigir esse problema, você deve adicionar um prefixo para o namespace de destino e usá-la para todas as referências globais e digite usos.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-265">To fix this, you must add a prefix for the target namespace and use that for all global references and type uses.</span></span> <span data-ttu-id="1ec9a-266">O esquema correto é semelhante ao seguinte.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-266">The corrected schema looks like the following.</span></span>
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"  
    xmlns:ns="http://ns" targetNamespace="http://ns" > 
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

<span data-ttu-id="1ec9a-267">Se seu esquema tiver o atributo **targetNamespace** especificado, certifique-se de que todas as referências globais estão qualificadas com o prefixo de namespace correto.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-267">If your schema has the **targetNamespace** attribute specified, ensure that all global references are qualified with the correct namespace prefix.</span></span> 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a><span data-ttu-id="1ec9a-268">A instrução codificação (Unicode versus ANSII) de processamento de XML</span><span class="sxs-lookup"><span data-stu-id="1ec9a-268">XML Processing Instruction Encoding (Unicode vs. ANSII)</span></span>

<span data-ttu-id="1ec9a-269">XML suporta apenas os conjuntos de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-269">XML supports only Unicode character sets.</span></span> <span data-ttu-id="1ec9a-270">Portanto, você poderá perder informações se salvar arquivos que usam ANSII caracteres.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-270">Therefore, you may lose information if you save files that use ANSII characters.</span></span> <span data-ttu-id="1ec9a-271">No entanto, o salvamento de arquivos como UTF-16 pode ser excessivo para seu uso específico.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-271">However, saving files as UTF-16 may be excessive for your particular use.</span></span> <span data-ttu-id="1ec9a-272">Para reduzir o custo de implementação de um leitor de XML, o autor XML deve estado qual codificação estão usando no nível superior XML instrução de processamento.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-272">To reduce the implementation cost of an XML reader, the XML author must state which encoding they are using in the top-level XML processing instruction.</span></span> <span data-ttu-id="1ec9a-273">Você pode reconhecer a seguinte instrução de processamento.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-273">You may recognize the following processing instruction.</span></span>
  
```XML
xml version="1.0" encoding="UTF-8"
```

<span data-ttu-id="1ec9a-274">Nesta marca de instrução de processamento Especifica que a codificação do arquivo é UTF-8.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-274">This processing instruction tag specifies that the encoding of the file is UTF-8.</span></span> <span data-ttu-id="1ec9a-275">Certifique-se de que a codificação do arquivo é o mesmo conforme a codificação mencionado na marca de instrução de processamento.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-275">You must ensure that the file encoding is the same as the encoding stated in the processing instruction tag.</span></span> <span data-ttu-id="1ec9a-276">Você pode determinar a codificação olhando os bytes do arquivo e procurando pelas marcas de ordem de byte Unicode.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-276">You can determine the encoding by looking at the bytes of the file and looking for the Unicode byte order marks.</span></span> <span data-ttu-id="1ec9a-277">Mas não há uma maneira mais fácil.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-277">But there is an easier way.</span></span> <span data-ttu-id="1ec9a-278">Se você tiver problemas ao abrir um esquema XSD, especificar a codificação como "UTF-8", abri-lo em um editor de texto como o bloco de notas e salve o arquivo usando a codificação UTF-8 (o bloco de notas fornece a lista suspensa **codificação** na caixa de diálogo **Salvar como** ).</span><span class="sxs-lookup"><span data-stu-id="1ec9a-278">If you have problems opening an XSD schema, specify the encoding as "UTF-8", open it in a text editor such as Notepad, and then save the file by using UTF-8 encoding (Notepad provides the **Encoding** drop-down list in the **Save As** dialog box).</span></span> <span data-ttu-id="1ec9a-279">Se você ainda tiver problemas ao abrir o arquivo, ele não é um problema de codificação.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-279">If you still have problems opening the file, it is not an encoding issue.</span></span> 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a><span data-ttu-id="1ec9a-280">maxOccurs atributo dentro do elemento xsd:all</span><span class="sxs-lookup"><span data-stu-id="1ec9a-280">maxOccurs Attribute Inside the xsd:all Element</span></span>

<span data-ttu-id="1ec9a-281">Devido à maneira nondeterminism definida na recomendação de esquema XML, o único valor válido para o atributo **maxOccurs** de um elemento **xsd: element** dentro de um elemento **xsd:all** é 1.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-281">Due to the way nondeterminism is defined in the XML Schema recommendation, the only valid value for the **maxOccurs** attribute of an **xsd:element** element inside an **xsd:all** element is 1.</span></span> <span data-ttu-id="1ec9a-282">Por exemplo, o seguinte é válido.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-282">For example, the following is valid.</span></span> 
  
```XML
<xsd:all> 
    <xsd:element name="x" minOccurs="0"/> 
    <xsd:element name="docs" minOccurs="0"/> 
</xsd:all> 

```

<span data-ttu-id="1ec9a-283">No entanto, este exemplo não é válido.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-283">However, this example is not valid.</span></span>
  
```XML
<xsd:all>     
    <xsd:element name="x" minOccurs="0" maxOccurs="unbounded"/> 
    <xsd:element name="docs" minOccurs="0" maxOccurs="unbounded"/> 
</xsd:all> 

```

<span data-ttu-id="1ec9a-284">Este exemplo é inválido porque o sistema de validação não pode determinar se dois ocorrências da `<x/>` mapa à declaração única ou para a declaração e outra definição inválida.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-284">This example is invalid because the validation system cannot determine whether two occurrences of  `<x/>` map to the single declaration or to the declaration and another invalid definition.</span></span> <span data-ttu-id="1ec9a-285">Sob a mesma perspectiva, você não pode ter dois elementos do mesmo nome em uma `<xsd:all>` marca.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-285">Along the same lines, you cannot have two elements of the same name in an  `<xsd:all>` tag.</span></span> 
  
<span data-ttu-id="1ec9a-286">Este exemplo também é interessante porque ela permite que você tenha qualquer número de `<x/>` e `<docs/>` nós dentro de um elemento contendo em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-286">This example is also interesting because it allows you to have any number of  `<x/>` and  `<docs/>` nodes inside a containing element in any order.</span></span> <span data-ttu-id="1ec9a-287">Embora essa construção for inválida, há uma solução alternativa.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-287">Although this construct is invalid, there is a workaround.</span></span> <span data-ttu-id="1ec9a-288">Usando o elemento **xsd:choice** , você pode obter o mesmo resultado, conforme demonstrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-288">By using the **xsd:choice** element, you can achieve the same result, as demonstrated in the following example.</span></span> 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a><span data-ttu-id="1ec9a-289">Como editar ou criar um XSD do InfoPath</span><span class="sxs-lookup"><span data-stu-id="1ec9a-289">How to Edit or Author an XSD for InfoPath</span></span>

<span data-ttu-id="1ec9a-290">Os dois exemplos nas seções a seguir mostram como editar ou criar um esquema para produzir resultados específicos no InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-290">The two examples in the following sections show how to edit or author a schema to produce specific results in InfoPath.</span></span>
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a><span data-ttu-id="1ec9a-291">Permitindo que os elementos definidos pelo usuário a ser inserido no painel de tarefas campos</span><span class="sxs-lookup"><span data-stu-id="1ec9a-291">Allowing User-defined Elements to Be Inserted in the Fields Task Pane</span></span>

<span data-ttu-id="1ec9a-292">Para permitir que os elementos definida pelo usuário seja exibido em um elemento pai no painel de tarefas **campos** , você deve inserir um **xsd: qualquer** elemento sob o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-292">To allow user-defined elements to appear under a parent element in the **Fields** task pane, you must insert an **xsd:any** element under the parent element.</span></span> <span data-ttu-id="1ec9a-293">Para permitir que os elementos definidos pelo usuário a ser inserido dentro `<your_node_name>` , a declaração de XSD deve se parecer com o seguinte.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-293">To allow user-defined elements to be inserted inside  `<your_node_name>` , the XSD declaration should resemble the following.</span></span> 
  
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

<span data-ttu-id="1ec9a-294">Se você também deseja permitir atributos definidos pelo usuário, você deve adicionar `<xsd:anyAttribute namespace="##any | ##other"/>` na declaração de elemento.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-294">If you also want to allow user-defined attributes, then you must add  `<xsd:anyAttribute namespace="##any | ##other"/>` to the element declaration.</span></span> 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a><span data-ttu-id="1ec9a-295">Permitindo que os elementos de texto Rich deve ser vinculada no Design do InfoPath e editar modos</span><span class="sxs-lookup"><span data-stu-id="1ec9a-295">Allowing Rich Text Elements to be Bound in InfoPath Design and Edit Modes</span></span>

<span data-ttu-id="1ec9a-296">Se você deseja declarar um elemento que pode ser vinculado a um controle de **Caixa de Rich Text** , então ela deve ter o seguinte formato, que inclui o **xsd: qualquer** elemento que possui um atributo de namespace definido como "http://www.w3.org/1999/xhtml" conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-296">If you want to declare an element that can be bound to a **Rich Text Box** control, then it should have the following form, which includes the **xsd:any** element that has a namespace attribute set to "http://www.w3.org/1999/xhtml" as shown in the following example.</span></span> 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3.org/1999/xhtml"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="conclusion"></a><span data-ttu-id="1ec9a-297">Conclusion</span><span class="sxs-lookup"><span data-stu-id="1ec9a-297">Conclusion</span></span>

<span data-ttu-id="1ec9a-298">Ao aproveitar o suporte do InfoPath para criar soluções de formulário XML que se baseiam em arquivos de esquema XML (. xsd) externamente criados, você pode criar um modelo de formulário que funciona com um esquema de padrão do setor ou um esquema personalizado criado por sua empresa ou organização.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-298">By taking advantage of InfoPath support for designing XML form solutions that are based on externally authored XML Schema (.xsd) files, you can create a form template that works with an industry-standard schema or custom schema created by your company or organization.</span></span> <span data-ttu-id="1ec9a-299">Usando as informações neste artigo, você pode criar arquivos de esquema XSD personalizados que são compatíveis com o InfoPath, e você pode solucionar problemas comuns que podem ocorrer quando você carregar arquivos XSD externamente criados no ambiente de design do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="1ec9a-299">By using the information in this article, you can create custom XSD schema files that are compatible with InfoPath, and you can troubleshoot common issues that you may encounter when you load externally authored XSD files into the InfoPath design environment.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1ec9a-300">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ec9a-300">See also</span></span>

- [<span data-ttu-id="1ec9a-301">Esquema XML do W3C</span><span class="sxs-lookup"><span data-stu-id="1ec9a-301">W3C XML Schema</span></span>](http://www.w3.org/XML/Schema)
- [<span data-ttu-id="1ec9a-302">Cartilha de esquema XML W3C</span><span class="sxs-lookup"><span data-stu-id="1ec9a-302">W3C XML Schema Primer</span></span>](http://www.w3.org/TR/xmlschema-0/)
- [<span data-ttu-id="1ec9a-303">Referência de estruturas de esquema do W3C XML</span><span class="sxs-lookup"><span data-stu-id="1ec9a-303">W3C XML Schema Structures Reference</span></span>](http://www.xml.com/pub/a/2000/11/29/schemas/structuresref.mdl)
- [<span data-ttu-id="1ec9a-304">Referência de tipos de dados de esquema do W3C XML</span><span class="sxs-lookup"><span data-stu-id="1ec9a-304">W3C XML Schema Datatypes Reference</span></span>](http://www.xml.com/pub/a/2000/11/29/schemas/dataref.mdl)
- [<span data-ttu-id="1ec9a-305">Tutorial do esquema XML</span><span class="sxs-lookup"><span data-stu-id="1ec9a-305">XML Schema Tutorial</span></span>](http://www.w3schools.com/schema/default.asp)
- [<span data-ttu-id="1ec9a-306">Central de desenvolvedores de XML</span><span class="sxs-lookup"><span data-stu-id="1ec9a-306">XML Developer Center</span></span>](http://msdn.microsoft.com/en-us/xml/default.aspx)

