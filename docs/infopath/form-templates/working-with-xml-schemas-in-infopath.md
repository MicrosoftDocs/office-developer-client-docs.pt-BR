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
# <a name="working-with-xml-schemas-in-infopath"></a>Trabalhar com esquemas XML no InfoPath

Um modelo de formulário criado com o Microsoft InfoPath usa um esquema XML (XSD) para executar validação estrutural e de dados no XML que é entrada, edição e saída de um formulário do InfoPath. Cada modelo de formulário criado no designer de formulário do InfoPath contém pelo menos um arquivo de esquema XSD (.xsd) usado para validação em tempo de executar.
  
> [!NOTE]
> As informações contidas neste tópico se aplica a modelos de formulário projetados para uso no editor do InfoPath. Modelos de formulário compatíveis com navegador têm requisitos de esquema XSD mais rígidos. Para obter mais informações, consulte a documentação sobre esquemas XML em modelos de formulário compatíveis com navegador disponíveis no MSDN. 
  
## <a name="using-externally-authored-xml-schemas"></a>Usando esquemas XML de autoria externa

Para carregar um arquivo de esquema XSD que foi de autoria fora do InfoPath, siga estas etapas.
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a>Para criar um modelo de formulário com base em um esquema externo

1. In the Backstage, click **New**, click **XML or Schema** under **Advanced Form Templates**, and then click **Design This Form**.
    
2. No Assistente **de Fonte** de Dados, especifique o arquivo de esquema XSD que você deseja usar e clique em **Próximo** e conclua as páginas restantes do assistente. 
    
## <a name="unsupported-xsd-constructs"></a>Construções XSD sem suporte

As seções a seguir descrevem construções XSD que o InfoPath não pode manipular em tempo de executar. Evite essas construções ao criar um modelo de formulário no designer de formulário do InfoPath.
  
## <a name="entity-and-entities-types"></a>Tipos de ENTIDADEs e ENTIDADEs

Os **tipos entity** e **ENTITIES** exigem uma DTD (definição de tipo de documento) para validação, que o InfoPath não dá suporte. O InfoPath não permite que você projete um modelo de formulário em relação a esse esquema e exibe uma mensagem de erro que recomenda alterar o tipo **ENTITY** para o tipo **NCName** do qual ENTITY **deriva.** 
  
> [!NOTE]
>  Se você criar manualmente um modelo de formulário do InfoPath fora do modo de design e ele usar um XSD que inclua tipos **entity** e **ENTITIES,** o modelo de formulário poderá funcionar em tempo de executar se o arquivo Template.xml contiver o DTD necessário para esses tipos. 
  
## <a name="required-xsdany-element"></a>Elemento xsd:any necessário

Uma ocorrência de um elemento **curinga xsd:any,** ou seja, uma ocorrência de um elemento **xsd:any** com um valor de atributo **minOccurs** maior que zero ("necessário qualquer"), impede que o InfoPath deterministicamente criar uma instância válida para esse fragmento de esquema. O InfoPath deve ser capaz de criar uma instância válida ao gerar um formulário que use esse fragmento de esquema. Como parte da execução do Assistente de Fonte de **Dados,** os esquemas com os elementos **xsd:any** necessários exigem que você escolha qual elemento de esquema deseja usar no lugar do elemento **xsd:any** necessário. 
  
## <a name="elements-with-an-abstract-complex-type"></a>Elementos com um tipo complexo abstrato

O modo de design do InfoPath dá suporte à criação de um modelo de formulário contra esquemas que usam tipos complexos abstratos. Por exemplo, se um elemento nomeado tem um tipo complexo abstrato chamado que tem duas derivações e  `shippingAddress`  `address` ,  `USAddress`  `CanadianAddress` InfoPath trata  `shippingAddress`  `shippingAddress`  `USAddress`  `shippingAddress` qualquer instância  `CanadianAddress` de como uma escolha entre com tipo e com tipo . Neste exemplo, se os esquemas fornecidos não contêm tipos derivados do endereço, o InfoPath solicita um esquema adicional que atende a esse requisito. 
  
## <a name="xsd-constructs-with-reduced-functionality"></a>Construções XSD com Funcionalidade Reduzida

As seções a seguir descrevem construções XSD que têm funcionalidade reduzida quando usadas para criar um modelo de formulário no designer de formulário do InfoPath.
  
## <a name="substitution-groups"></a>Grupos de substituição

Todos os membros do grupo de substituição aparecem no painel **de tarefas** Campos. O InfoPath representa as possibilidades de substituição como uma escolha de todos os grupos de substituição (incluindo o elemento de definição, se não for abstrato). Se não houver grupos de substituição para um elemento abstrato, o InfoPath solicitará que você forneça um esquema que contenha pelo menos um elemento que seja um grupo de substituição. 
  
## <a name="unbounded-choice-elements"></a>Elementos de escolha não acondido

O fragmento de esquema a seguir mostra um elemento de escolha nãobounded:
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

O InfoPath exibe elementos de escolha repetidos como opções repetidas no painel **de** tarefas Campos. Há um controle grupo de **escolha** de repetição que você pode usar para representar a lista heterogênea definida pelo elemento de opção de repetição no XSD. 
  
## <a name="repeating-sequence"></a>Sequência de repetição

O fragmento de esquema a seguir mostra uma sequência de repetição:
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

Desde que a sequência de repetição contenha um elemento necessário, o InfoPath carrega o XSD sem modificá-lo e permite vincular controles de seção repetitivas à sequência de repetição.
  
## <a name="choice-of-model-groups"></a>Escolha de grupos de modelos

O fragmento de esquema a seguir mostra o elemento de escolha que contém vários grupos de modelos:
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

O modo de design do InfoPath dá suporte a tais construções XSD sem a necessidade de qualquer modificação feita pelo designer de formulário. Embora o InfoPath não modifique o significado do esquema, ele simplifica o constructo de escolha acima em uma única opção recolhido equivalente no painel de tarefas Campos.  
  
## <a name="optional-sibling-with-same-qualified-name"></a>Irmão opcional com o mesmo nome qualificado

O fragmento de esquema a seguir mostra um irmão opcional com o mesmo nome qualificado ( `QName` ):
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

**Expressões XPath** para esses nós podem ser complexas porque cada instância XML potencial deve ser contabilada no designer de formulário do InfoPath. O InfoPath não expõe partes do esquema para o qual ele pode ter dificuldade para criar ligações **XPath** corretas. Os avisos são exibidos em relação às partes do esquema que são ignoradas. 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a>Construções XSD com significado especial no InfoPath

As seções a seguir descrevem construções XSD que têm significado especial quando usadas na criação de um modelo de formulário no modo de design. Estas seções descrevem como você pode usar as construções em seu esquema para habilitar determinados comportamentos.
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a>Adicionando novos campos e grupos de elementos com o painel de tarefas Fields

Você pode construir seu esquema para que possa usar o painel de tarefas **Campos** para adicionar novos campos e grupos de elementos a um elemento em tempo de design. Para fazer isso, você declara um elemento em seu esquema com um elemento **xsd:any** opcional não-bounded que especifica o atributo de namespace com o caractere **curinga ##any.** Em seguida, no modo de design, você pode usar o painel de tarefas **Campos** para adicionar novos campos e grupos de elementos a esse elemento. Por exemplo, você poderia adicionar novo conteúdo ao seguinte elemento: 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a>Adicionando novos campos de atributo com o painel de tarefas Fields

Da mesma forma que o caso do elemento, você pode declarar um atributo com um elemento **anyAttribute** que tenha o atributo namespace especificado como o caractere curinga **##any.** No tempo de design, você pode usar o painel de tarefas **Fields** para adicionar novo conteúdo a esse atributo de esquema. 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a>Armazenar assinaturas XML na fonte de dados

Para permitir que os usuários assinem digitalmente um formulário em tempo de executar, o esquema da fonte de dados deve declarar um elemento nomeado assinatura para armazenar as informações de assinaturas XML (assinatura digital) criadas quando um usuário assina o formulário. Faça essa declaração usando o elemento **xsd:any** com o atributo namespace especificado como o namespace de Assinaturas XML com um caractere curinga, da seguinte forma: https://www.w3c.org/2000/09/xmldsig# " 
  
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

## <a name="binding-a-field-to-a-rich-text-box-control"></a>Binding a Field to a Rich Text Box Control

 **Os controles Rich Text Box** no InfoPath geram XHTML genérico; consequentemente, seu esquema deve especificar que qualquer número de texto e nós XHTML é válido no XML da instância do formulário. Você pode obter essa especificação com o seguinte constructo XSD: 
  
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
> O InfoPath nunca modifica o conteúdo do arquivo de esquema (.xsd), mas pode inferir logicamente um subconjunto dele para fins de design. O arquivo de esquema é sempre intocado dentro do modelo de formulário no tempo de design e no tempo de executar. 
  
## <a name="debugging-common-xsd-errors"></a>Depurando erros comuns de XSD

Se você carregar arquivos XSD criado externamente para criar modelos de formulário no designer de formulário do InfoPath, poderá receber um dos dois tipos de mensagens de erro: mensagens de erro MSXML ou mensagens de erro do InfoPath. As mensagens de erro MSXML aparecem na seção Detalhes de uma caixa de diálogo de mensagem de erro do InfoPath e sempre começam com uma referência ao nome ou caminho do arquivo de esquema que está aparecendo o erro.  Algumas construções válidas de esquema XSD não são suportadas pelo InfoPath; eles são discutidos na seção Unsupported XSD Constructs. As seções a seguir descrevem alguns erros comuns que podem fazer com que os esquemas não carreguem com êxito no InfoPath. 
  
## <a name="the-xsd-namespace-declaration"></a>A declaração de namespace XSD

Semelhante a todos os padrões W3C, os esquemas XML (XSD) passaram por um processo de revisão demorado em sua maneira de se tornar uma recomendação. Havia muitos rascunhos de trabalho e, consequentemente, muitos arquivos XSD foram escritos com base nesses padrões em evolução. Durante esse processo, a Microsoft criou uma linguagem de esquema proprietária chamada XML-Data Reduced (XDR) incluída no MSXML 3.0. A partir do lançamento do MSXML 4.0, o Microsoft XML Core Services dá suporte à recomendação completa do XSD. Muitos programas para a criação de esquemas não aguardaram até que o XSD se torne uma recomendação completa. Versões mais antigas desses programas podem produzir arquivos XSD desatualizados aos quais a infraestrutura MSXML 5.0, da qual depende o InfoPath, não dá suporte.
  
Para garantir que um arquivo XSD suporte a recomendação XSD completa, ele deve conter a seguinte declaração de namespace XML na marca \< de \> esquema:
  
```XML
xmlns:xsd="https://www.w3.org/2001/XMLSchema"
```

Semelhante a todas as declarações de namespace XML, o prefixo XML (neste caso ' xsd') pode ser qualquer cadeia de caracteres de prefixo válida. Alguns prefixos comuns que você pode ver na prática são 'xsd', 'xs' e '' (sem prefixo). O MSXML geralmente relata um erro sobre a raiz não estar sendo definida corretamente se essa declaração de namespace estiver ausente.
  
## <a name="importing-and-including-schemas"></a>Importando e incluindo esquemas

Os esquemas XSD são extensíveis e podem importar e incluir outros esquemas. Geralmente, você deve importar um esquema se o esquema especificado no atributo **targetNamespace** for diferente do esquema atual. Você deve incluí-lo se o esquema especificado no atributo **targetNamespace** for o mesmo que o esquema atual. 
  
A semântica para importação e inclusão de esquemas é a seguinte:
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

Se o **atributo schemaLocation** estiver ausente (como acontece com alguns conversores), MSXML gera um erro porque não consegue encontrar o arquivo. Se você receber esse erro, verifique também se o recurso ou o local especificado no atributo schemaLocation está acessível pelos usuários do modelo de formulário. Obviamente, ocorrerão erros se o atributo **schemaLocation** fizer referência a um servidor ou diretório que está ino mesmo ou inexistente ou se os usuários não têm permissões de acesso. Além disso, examine todos os esquemas importados e incluídos para garantir que sejam válidos. 
  
> [!NOTE]
> Erros causados por problemas com o **atributo schemaLocation** são um problema apenas quando o InfoPath importa os esquemas pela primeira vez; ou seja, quando você começa a criar um formulário com base em um esquema existente. Depois disso, o InfoPath funciona com versões armazenadas em cache dos arquivos de esquema armazenados no modelo de formulário. 
  
Um atributo de namespace vazio é permitido ao importar um esquema, se esse esquema não especificar um **atributo targetNamespace.** Em geral, o namespace na importação deve corresponder ao **targetNamespace** especificado no esquema que você importa. 
  
## <a name="nondeterministic-schemas"></a>Esquemas não determinísticos

A infraestrutura MSXML 5.0 da qual o InfoPath depende pode detectar e aumentar erros de forma confiável para alertá-lo sobre esquemas não determinísticos, mas a mensagem de erro resultante não fornece um número de linha para dizer qual parte do esquema está aprindo o erro. Esta seção discute por que é importante que os arquivos de esquema XSD sejam determinísticos e o que significa não ser determinístico. Ele também mostra alguns erros comuns a evitar.
  
Os esquemas XSD existem para validar a semântica de tipos e a estrutura de dados XML. Para realizar essa tarefa, o sistema de validação (neste caso, MSXML 5.0) deve mapear nós XML para declarações XSD. Sem esse mapeamento, o sistema de validação não pode realizar sua tarefa. Se um mapeamento puder ser garantido, o esquema será determinístico. Se houver uma única instância XML que torna esse mapeamento impossível, o esquema não é determinístico.
  
O esquema de exemplo a seguir não é determinístico:
  
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

Para ilustrar por que esse segmento XSD não é determinístico, suponha que você tenha o fragmento XML a seguir que deseja validar com este esquema:
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

Nesse fragmento XML, não está claro se o elemento *\< file_path \>* é o nó necessário da primeira parte da declaração de escolha ou o opcional da segunda parte da declaração de escolha. Essa distinção é importante pelos seguintes motivos: 
  
1. Se o fragmento XML for validado em relação à primeira parte da declaração de escolha, o XML será válido em relação ao esquema.
    
2. Se o fragmento XML for validado em relação à segunda parte da declaração de escolha, o esquema não será válido, pois o nó \< de URI \> necessário está ausente. 
    
Alguns sistemas de validação XSD erram em relação à validação desse esquema porque há um caminho válido. O MSXML é mais estrito e gera um erro informando que o esquema não é determinístico.
  
A seguir estão alguns exemplos de esquemas não determinísticos. A primeira lida com elementos opcionais. Esses casos geralmente surgem de XDR para conversores XSD devido a diferenças nas cardinalidades padrão nas duas linguagens de esquema. O primeiro caso a ser considerado são elementos opcionais declarados com **elementos xsd:choice** e **xsd:sequence.** Elementos opcionais declarados em um elemento **xsd:sequence** geralmente são validados corretamente, desde que você não tenha elementos com o mesmo nome mais de uma vez, com apenas elementos opcionais entre eles. Por exemplo: 
  
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

Para entender por que esse segmento de esquema não é determinístico, suponha que você tenha o seguinte fragmento XML inválido:
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
    <anotherNode/> 
</container> 

```

Ao olhar para esse fragmento, você pode ver por que ele é inválido: há dois elementos antes do elemento, quando  `<aNode>` apenas um é  `<anotherNode>` permitido. 
  
Agora, suponha que você tenha a seguinte instância XML para validar:
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

O desafio é determinar se essa instância é válida. Você tem dois elementos onde apenas um é permitido ou você tem um elemento onde ele é permitido e  `<aNode>` outro onde ele é  `<aNode>` permitido? O esquema não é determinístico porque não há como saber. 
  
Da mesma forma, elementos opcionais declarados em um **elemento xsd:choice** geralmente são problemáticos. No exemplo simplificado a seguir, não há nenhuma maneira de determinar se a escolha ocorreu uma vez com o elemento opcional não estando lá ou se ela nunca ocorreu. 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

A prática questionável final é usar um **elemento xsd:any** sem uma definição de namespace, como em , após um `<xsd:any namespace="##other"/>` elemento **xsd:sequence.** Essa construção é especialmente problemática quando segue um elemento opcional. Se você revisitar o exemplo anterior e alterar apenas o último nó para um elemento **xsd:any,** poderá ver que todos os argumentos anteriores sobre nondeterminismo ainda se aplicam, da seguinte maneira: 
  
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

## <a name="illegal-enumeration-values"></a>Valores de enumeração ilegais

Esquemas XSD normalmente não executam nenhuma validação de tipo até que você valide um documento de instância real. Uma exceção a isso é quando você tem uma enumeração em seu esquema. Nesse caso, o esquema valida os valores de enumeração em relação aos tipos de enumeração para garantir que sejam valores de nó adequados. Aqui estão dois exemplos:
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

Esse esquema é inválido porque "horário da manhã" não é um valor válido para um elemento do tipo **xsd:time**.
  
Veja a seguir um exemplo mais complexo:
  
```XML
<xsd:simpleType name="concession"> 
    <xsd:restriction base="xsd:NMTOKEN"> 
        <xsd:enumeration value="GummyBears"/> 
        <xsd:enumeration value="SnowCaps"/> 
        <xsd:enumeration value="M&Ms"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

Para entender por que este exemplo é inválido, você deve entender como o tipo **xsd:NMTOKEN** é definido. A especificação de tipos de dados W3C define o tipo **NMTOKEN** da seguinte forma: "Um NMTOKEN (token de nome) é qualquer mistura de caracteres de nome". 
  
Se você investigar mais, descobrirá que "&" não é um caractere de nome válido e, portanto, "M&Ms" não valida como um tipo **NMTOKEN.** 
  
## <a name="empty-sequence-or-choice-elements"></a>Elementos de sequência ou escolha vazios

Às vezes, o MSXML gera erros sobre declarações de esquema que contêm elementos **xsd:choice** ou **xsd:sequence** vazios, conforme mostrado no exemplo a seguir. 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

Remover a marca  `<xsd:choice />` vazia deve resolver esse problema. 
  
## <a name="regular-expressions"></a>Expressões Regulares

O MSXML 5.0 pode ter problemas para validar padrões de expressões regulares durante o carregamento. Expressões regulares podem ser complicadas e você deve ter cuidado ao usá-las. Cada analisador XSD parece ter linguagens de expressões regulares flexíveis; ou seja, eles implementam a linguagem oficial de expressão regular XSD, além de elementos de outras linguagens de expressão regular. Se o designer de formulário do InfoPath tiver problemas para analisar uma expressão regular, os dados de exemplo gerados pelo InfoPath poderão ser inválidos ou podem não ser gerados. Isso é aceitável no tempo de design, pois o InfoPath usa apenas dados de exemplo para formatação. No entanto, se você usar uma expressão regular que o MSXML não suporta, o InfoPath não poderá validar um valor em relação a ele quando um usuário estiver preenchendo um formulário. [Xml Schema Part 0: Primer Second Edition](https://www.w3.org/TR/xmlschema-0/)describes what is supported in XSD regular expressions. Para obter mais informações sobre expressões regulares XSD e expressões regulares Unicode nível 1, consulte [Expressões regulares Unicode.](https://www.unicode.org/reports/tr18/) 
  
## <a name="targetnamespace-attribute-issues"></a>Problemas de atributo targetNamespace

O XSD é interessante porque, por padrão, o atributo **targetNamespace** refere-se apenas às declarações de nível superior, embora você possa definir e substituir esse  `attributeFormDefault=qualified`  `elementFormDefault=qualified` comportamento padrão. Por exemplo, suponha que você tenha o seguinte XSD. 
  
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

E que seu documento de instância XML se parece com o exemplo a seguir.
  
```XML
<ns:root xmlns:ns="https://ns"> 
    <local/> 
</ns:root> 

```

As definições locais não exigem o namespace de destino porque a qualificação está desligada por padrão. No entanto, se você alterar sua definição local para global, sua referência deverá ser qualificada com o prefixo de namespace. Por exemplo, o esquema a seguir é inválido.
  
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

Esse esquema é inválido porque "global" está no namespace " https://ns ". O ref="global" simples não é reconhecido porque o namespace padrão não é " https://ns ". Para corrigir isso, você deve adicionar um prefixo para o namespace de destino e usá-lo para todas as referências globais e usos de tipo. O esquema corrigido é parecido com o seguinte.
  
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

Se o esquema tiver o **atributo targetNamespace** especificado, certifique-se de que todas as referências globais sejam qualificadas com o prefixo de namespace correto. 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a>Codificação de instrução de processamento XML (Unicode versus ANSII)

XML oferece suporte apenas a conjuntos de caracteres Unicode. Portanto, você pode perder informações se salvar arquivos que usam caracteres ANSII. No entanto, salvar arquivos como UTF-16 pode ser excessivo para seu uso específico. Para reduzir o custo de implementação de um leitor de XML, o autor xml deve dizer qual codificação eles estão usando na instrução de processamento XML de nível superior. Você pode reconhecer a instrução de processamento a seguir.
  
```XML
xml version="1.0" encoding="UTF-8"
```

Essa marca de instrução de processamento especifica que a codificação do arquivo é UTF-8. Você deve garantir que a codificação do arquivo seja a mesma que a codificação indicado na marca de instrução de processamento. Você pode determinar a codificação observando os bytes do arquivo e procurando as marcas de ordem de bytes Unicode. Mas há uma maneira mais fácil. Se você tiver problemas para abrir um esquema XSD, especifique a codificação como "UTF-8", abra-a em um editor de texto como o  Bloco de Notas e salve  o arquivo usando a codificação UTF-8 (o Bloco de Notas fornece a lista de codificação na caixa de diálogo Salvar como). Se você ainda tiver problemas para abrir o arquivo, não será um problema de codificação. 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a>Atributo maxOccurs dentro do elemento xsd:all

Devido à maneira como o nondeterminismo é definido na recomendação de esquema XML, o único valor válido para o atributo **maxOccurs** de um elemento **xsd:element** dentro de um elemento **xsd:all** é 1. Por exemplo, o seguinte é válido. 
  
```XML
<xsd:all> 
    <xsd:element name="x" minOccurs="0"/> 
    <xsd:element name="docs" minOccurs="0"/> 
</xsd:all> 

```

No entanto, este exemplo não é válido.
  
```XML
<xsd:all>     
    <xsd:element name="x" minOccurs="0" maxOccurs="unbounded"/> 
    <xsd:element name="docs" minOccurs="0" maxOccurs="unbounded"/> 
</xsd:all> 

```

Este exemplo é inválido porque o sistema de validação não pode determinar se duas ocorrências de mapa para a declaração única ou para a declaração  `<x/>` e outra definição inválida. Nas mesmas linhas, não é possível ter dois elementos com o mesmo nome em uma  `<xsd:all>` marca. 
  
Este exemplo também é interessante porque permite que você tenha qualquer número de nós dentro de um elemento que o contém  `<x/>`  `<docs/>` em qualquer ordem. Embora essa construção seja inválida, há uma solução alternativa. Usando o **elemento xsd:choice,** você pode obter o mesmo resultado, conforme demonstrado no exemplo a seguir. 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a>Como editar ou editar um XSD para InfoPath

Os dois exemplos nas seções a seguir mostram como editar ou gerar um esquema para produzir resultados específicos no InfoPath.
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a>Permitindo que elementos definidos pelo usuário sejam inseridos no painel de tarefas Fields

Para permitir que elementos definidos pelo usuário apareçam em um elemento pai no painel de tarefas **Fields,** você deve inserir um elemento **xsd:any** sob o elemento pai. Para permitir que elementos definidos pelo usuário sejam inseridos dentro , a declaração  `<your_node_name>` XSD deve se parecer com o seguinte. 
  
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

Se você também quiser permitir atributos definidos pelo usuário, deverá adicionar  `<xsd:anyAttribute namespace="##any | ##other"/>` à declaração do elemento. 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a>Permitindo que elementos rich text sejam vinculados em modos de edição e design do InfoPath

Se você deseja declarar um elemento que pode ser vinculado a um controle **Rich Text Box,** ele deve ter o seguinte formulário, que inclui o elemento **xsd:any** que tem um atributo de namespace definido como " " conforme mostrado no exemplo a https://www.w3.org/1999/xhtml seguir. 
  
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

## <a name="conclusion"></a>Conclusão

Ao aproveitar o suporte do InfoPath para projetar soluções de formulário XML baseadas em arquivos de esquema XML (.xsd) criados externamente, você pode criar um modelo de formulário que funciona com um esquema padrão do setor ou um esquema personalizado criado por sua empresa ou organização. Usando as informações deste artigo, você pode criar arquivos de esquema XSD personalizados compatíveis com o InfoPath e solucionar problemas comuns que você pode encontrar ao carregar arquivos XSD criado externamente no ambiente de design do InfoPath.
  
## <a name="see-also"></a>Confira também

- [Esquema XML W3C](https://www.w3.org/XML/Schema)
- [Manual de esquema XML W3C](https://www.w3.org/TR/xmlschema-0/)
- [Referência de estruturas de esquema XML W3C](https://www.xml.com/pub/a/2000/11/29/schemas/structuresref.html)
- [Referência de datatypes de esquema XML W3C](https://www.xml.com/pub/a/2000/11/29/schemas/dataref.html)
- [Tutorial de esquema XML](https://www.w3schools.com/xml/schema_intro.asp)
- [Central de Desenvolvedores XML](https://msdn.microsoft.com/xml/default.aspx)

