---
title: Trabalhar com esquemas XML no InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c1d70e9f-b9fc-7bdb-107e-d0cd8191607b
description: Um modelo de formulário que você cria com o Microsoft InfoPath usa um XSD (esquema XML) para executar a validação estrutural e de dados no XML que é de entrada, editada e de saída de um formulário do InfoPath. Todos os modelos de formulário criados no designer de formulários do InfoPath contêm pelo menos um arquivo de esquema XSD (. xsd) usado para validação no tempo de execução.
ms.openlocfilehash: 25828c3ec21d22a9952452d5a82fe1a3b4bab54c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303161"
---
# <a name="working-with-xml-schemas-in-infopath"></a>Trabalhar com esquemas XML no InfoPath

Um modelo de formulário que você cria com o Microsoft InfoPath usa um XSD (esquema XML) para executar a validação estrutural e de dados no XML que é de entrada, editada e de saída de um formulário do InfoPath. Todos os modelos de formulário criados no designer de formulários do InfoPath contêm pelo menos um arquivo de esquema XSD (. xsd) usado para validação no tempo de execução.
  
> [!NOTE]
> As informações contidas neste tópico se aplicam aos modelos de formulário projetados para uso no editor do InfoPath. Modelos de formulário compatíveis com o navegador têm requisitos de esquema XSD mais estritos. Para obter mais informações, consulte a documentação sobre esquemas XML em modelos de formulário compatíveis com o navegador, disponíveis no MSDN. 
  
## <a name="using-externally-authored-xml-schemas"></a>Usando esquemas XML criados externamente

Para carregar um arquivo de esquema XSD que foi criado fora do InfoPath, siga estas etapas.
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a>Para criar um modelo de formulário com base em um esquema externo

1. No Backstage, clique em **novo**, em **XML ou esquema** em **modelos de formulário avançados**e, em seguida, clique em **criar este formulário**.
    
2. No **Assistente de fonte de dados**, especifique o arquivo de esquema XSD que você deseja usar e clique em **Avançar** e preencha as páginas restantes do assistente. 
    
## <a name="unsupported-xsd-constructs"></a>Construções XSD sem suporte

As seções a seguir descrevem as construções XSD que o InfoPath não pode manipular no tempo de execução. Evite essas construções ao criar um modelo de formulário no designer de formulários do InfoPath.
  
## <a name="entity-and-entities-types"></a>Tipos de entidade e entidades

Os tipos **Entity** e **Entities** exigem uma definição de tipo de documento (DTD) para validação, para a qual o InfoPath não oferece suporte. O InfoPath não permite que você projete um modelo de formulário em relação a um esquema e exibe uma mensagem de erro que recomenda alterar o tipo de **entidade** para o tipo **NCName** a partir do qual a **entidade** deriva. 
  
> [!NOTE]
>  Se você criar manualmente um modelo de formulário do InfoPath fora do modo de design e usar um XSD que inclua entidades **** e tipos de **entidade** , o modelo de formulário pode funcionar em tempo de execução se o arquivo template. XML contiver o DTD necessário para esses tipos. 
  
## <a name="required-xsdany-element"></a>XSD obrigatório: qualquer elemento

Uma ocorrência de um **xsd: qualquer** elemento curinga, ou seja, uma ocorrência de um elemento **xsd: any** com um valor de atributo **minOccurs** maior que zero ("required any"), impede que o InfoPath crie uma instância válida para Este fragmento de esquema. O InfoPath deve ser capaz de criar uma instância válida ao gerar um formulário que usa esse fragmento de esquema. Como parte da execução do **Assistente de fonte de dados**, os esquemas com o **XSD obrigatório: qualquer** elemento exigem que você escolha qual elemento do esquema você deseja usar no lugar do elemento **xsd: any** necessário. 
  
## <a name="elements-with-an-abstract-complex-type"></a>Elementos com um tipo complexo abstrato

O modo de design do InfoPath oferece suporte ao design de um modelo de formulário em esquemas que usam tipos complexos abstratos. Por exemplo, se um elemento chamado `shippingAddress` tem um tipo complexo abstrato chamado `address` que tem duas derivações, `USAddress` e `CanadianAddress`o InfoPath trata qualquer instância de `shippingAddress` como uma opção entre `shippingAddress` com tipo `USAddress` e `shippingAddress` com tipo `CanadianAddress` . Neste exemplo, se os esquemas fornecidos não contiverem tipos que derivem de endereço, o InfoPath solicitará um esquema adicional que atenda a esse requisito. 
  
## <a name="xsd-constructs-with-reduced-functionality"></a>Construções XSD com funcionalidade reduzida

As seções a seguir descrevem construções XSD que têm funcionalidade reduzida quando usadas para criar um modelo de formulário no designer de formulários do InfoPath.
  
## <a name="substitution-groups"></a>Grupos de substituição

Todos os membros do grupo de substituição aparecem no painel de tarefas **campos** . O InfoPath representa as possibilidades de substituição como uma opção de todos os grupos de substituição (incluindo o elemento de definição, se não for abstrato). Se não houver grupos de substituição para um elemento abstrato, o InfoPath solicitará que você forneça um esquema que contenha pelo menos um elemento que seja um grupo de substituição. 
  
## <a name="unbounded-choice-elements"></a>Elementos Choice não vinculados

O seguinte fragmento de esquema mostra um elemento Choice não associado:
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

O InfoPath exibe elementos de escolha de repetição como opções repetidas no painel de tarefas **campos** . Há um controle de **grupo de escolha de repetição** que pode ser usado para representar a lista heterogênea definida pelo elemento Choice de repetição no XSD. 
  
## <a name="repeating-sequence"></a>Sequência repetitiva

O seguinte fragmento de esquema mostra uma sequência repetitiva:
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

Contanto que a sequência repetitiva contenha um elemento Required, o InfoPath carregará o XSD sem modificá-lo e permitirá que você vincule os controles de seção de repetição à sequência de repetição.
  
## <a name="choice-of-model-groups"></a>Escolha de grupos de modelos

O seguinte fragmento de esquema mostra o elemento Choice contendo vários grupos de modelos:
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

O modo de design do InfoPath oferece suporte a essas construções XSD sem exigir qualquer modificação pelo designer de formulários. Embora o InfoPath não modifique o significado do esquema, ele simplifica a construção de escolha acima em uma única opção recolhida, contraída, no painel de tarefas **campos** . 
  
## <a name="optional-sibling-with-same-qualified-name"></a>Irmão opcional com o mesmo nome qualificado

O seguinte fragmento de esquema mostra um irmão opcional com o mesmo nome`QName`qualificado ():
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

As expressões **XPath** desses nós podem ser complexas, pois cada instância XML potencial deve ser contabilizada no designer de formulários do InfoPath. O InfoPath não expõe partes do esquema para as quais pode ter dificuldade para criar associações **XPath** corretas. Os avisos aparecem sobre as partes do esquema que são ignoradas. 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a>Construções XSD com significado especial no InfoPath

As seções a seguir descrevem construções XSD que têm um significado especial quando usadas na criação de um modelo de formulário no modo de design. Estas seções descrevem como você pode usar as construções em seu esquema para habilitar determinados comportamentos.
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a>Adição de novos campos e grupos de elementos com o painel de tarefas campos

Você pode construir seu esquema para que você possa usar o **** painel de tarefas Fields para adicionar novos campos de elemento e grupos a um elemento no tempo de design. Para fazer isso, você declara um elemento no seu esquema com um elemento **xsd: any** opcional, não associado, que especifica o atributo namespace com o curinga **# #any** . Em seguida, no modo de design, você pode usar o painel de tarefas **campos** para adicionar novos campos e grupos ao elemento. Por exemplo, você pode adicionar novo conteúdo ao seguinte elemento: 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a>Adição de novos campos de atributo com o painel de tarefas campos

Da mesma forma que o elemento Case, você pode declarar um atributo com um elemento **anyAttribute** que tem o atributo namespace especificado como o caractere curinga **# #any** . No tempo de design, você pode usar o painel de tarefas **campos** para adicionar novo conteúdo a esse atributo de esquema. 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a>Armazenar assinaturas XML na fonte de dados

Para permitir que os usuários assinem um formulário digitalmente em tempo de execução, o esquema da fonte de dados deve declarar um elemento chamado Signature para armazenar as assinaturas XML (assinatura digital) que são criadas quando um usuário assina o formulário. Você faz essa declaração usando o elemento **xsd: any** com o atributo namespace especificado como namespace de assinaturas XML com um caractere curinga, da seguinte maneira: "https://www.w3c.org/2000/09/xmldsig#" 
  
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

## <a name="binding-a-field-to-a-rich-text-box-control"></a>Vincular um campo a um controle de caixa de Rich Text

 Os controles de **caixa de Rich Text** no InfoPath geram XHTML genérico; Consequentemente, o esquema deve especificar que qualquer número de texto e nós XHTML é válido no XML da instância do formulário. Você pode obter essa especificação com a seguinte construção XSD: 
  
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
> O InfoPath nunca modifica o conteúdo do arquivo de esquema (. xsd), mas pode inferir logicamente um subconjunto de ti para fins de design. O arquivo de esquema está sempre intocado no modelo de formulário no tempo de design e no tempo de execução. 
  
## <a name="debugging-common-xsd-errors"></a>Depuração de erros XSD comuns

Se você carregar arquivos XSD criados externamente para criar modelos de formulário no designer de formulários do InfoPath, poderá receber um dos dois tipos de mensagens de erro: mensagens de erro do MSXML ou mensagens de erro do InfoPath. As mensagens de erro do MSXML aparecem na seção **detalhes** de uma caixa de diálogo de mensagem de erro do InfoPath e sempre começam com uma referência ao nome ou caminho do arquivo de esquema que está gerando o erro. Algumas construções de esquema XSD válidas não são suportadas pelo InfoPath; Eles são discutidos na seção construções XSD não suportadas. As seções a seguir descrevem alguns erros comuns que podem fazer com que os esquemas falhem ao carregar com êxito no InfoPath. 
  
## <a name="the-xsd-namespace-declaration"></a>A declaração de namespace XSD

Da mesma forma que todos os padrões do W3C, os esquemas XML (XSD) passaram por um processo de revisão demorado, para se tornar uma recomendação. Havia vários rascunhos de trabalho e, consequentemente, muitos arquivos XSD foram escritos com base nesses padrões em expansão. Durante esse processo, a Microsoft criou um idioma de esquema proprietário chamado XML-Data reDuced (XDR) que foi incluído no MSXML 3,0. A partir da versão do MSXML 4,0, o Microsoft XML Core Services oferece suporte a todas as recomendações do XSD. Muitos programas para a criação de esquemas não aguardaram que o XSD se tornasse uma recomendação completa. Versões mais antigas desses programas podem produzir arquivos XSD desatualizados que a infraestrutura de MSXML 5,0, na qual o InfoPath depende, não oferece suporte.
  
Para garantir que um arquivo XSD dê suporte à recomendação XSD completa, ele deve conter a seguinte declaração de namespace XML \<na\> marca de esquema:
  
```XML
xmlns:xsd="https://www.w3.org/2001/XMLSchema"
```

Semelhante a todas as declarações de namespace XML, o prefixo XML (neste caso ' XSD ') pode ser qualquer cadeia de caracteres de prefixo válida. Alguns prefixos comuns que você pode ver na prática são ' XSD ', ' XS ' e ' ' (sem prefixo). O MSXML geralmente relata um erro sobre a raiz não estar definida corretamente se essa declaração de namespace estiver ausente.
  
## <a name="importing-and-including-schemas"></a>Importar e incluir esquemas

Os esquemas XSD são extensíveis e podem importar e incluir outros esquemas. Geralmente, você deve importar um esquema se o esquema especificado no atributo **targetNamespace** for diferente do esquema atual. Você deve incluí-lo se o esquema especificado no atributo **targetNamespace** for igual ao esquema atual. 
  
As semânticas para importar e incluir esquemas são as seguintes:
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

Se o atributo **schemaLocation** estiver ausente (como acontece com alguns conversores), o MSXML gerará um erro porque não consegue encontrar o arquivo. Se você receber esse erro, verifique também se o recurso ou o local especificado no atributo schemaLocation é acessível por usuários do modelo de formulário. Obviamente, ocorrerão erros se o atributo **schemaLocation** fizer referência a um servidor ou diretório inoperante ou não existente, ou se os usuários não tiverem permissões de acesso. Além disso, certifique-se de examinar todos os esquemas importados e incluídos para garantir que eles sejam válidos. 
  
> [!NOTE]
> Os erros causados por problemas com o atributo **schemaLocation** são um problema somente quando o InfoPath importa os esquemas pela primeira vez; ou seja, quando você começar a criar um formulário pela primeira vez com base em um esquema existente. Depois, o InfoPath funciona com versões em cache dos arquivos de esquema armazenados no modelo de formulário. 
  
Um atributo de namespace vazio é permitido ao importar um esquema, se esse esquema não especificar um atributo **targetNamespace** . Em geral, o namespace na importação deve corresponder ao **targetNamespace** especificado no esquema que você importou. 
  
## <a name="nondeterministic-schemas"></a>Esquemas não determinísticos

A infraestrutura de MSXML 5,0 com a qual o InfoPath depende pode detectar e gerar erros de forma confiável para o alerta para esquemas não determinísticos, mas a mensagem de erro resultante não fornece um número de linha para informá-lo que parte do esquema está gerando o erro. Esta seção discute por que é importante que os arquivos do esquema XSD sejam determinísticos e o que significa ser não determinístico. Também mostra alguns erros comuns a serem evitados.
  
Há esquemas XSD para fins de validação da estrutura de dados XML e da semântica de tipo. Para realizar essa tarefa, o sistema de validação (neste caso, MSXML 5,0) deve mapear nós XML para declarações XSD. Sem esse mapeamento, o sistema de validação não pode realizar a tarefa. Se um mapeamento puder ser garantido, o esquema será determinístico. Se houver uma única instância XML que torne esse mapeamento impossível, o esquema não será determinístico.
  
O seguinte esquema de exemplo não é determinístico:
  
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

Para ilustrar por que esse segmento XSD não é determinístico, suponha que você tenha o seguinte fragmento de XML que você deseja validar com este esquema:
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

Nesse fragmento XML, não fica claro se o * \<elemento file_path\> * é o nó obrigatório da primeira parte da declaração Choice ou o opcional da segunda parte da declaração Choice. Essa distinção é importante pelos seguintes motivos: 
  
1. Se o fragmento XML for validado em relação à primeira parte da declaração Choice, o XML será válido em relação ao esquema.
    
2. Se o fragmento XML for validado com base na segunda parte da declaração Choice, o esquema não é válido, pois o nó \<URI\> necessário está ausente. 
    
Alguns sistemas de validação XSD não são validados em relação a esse esquema porque há um caminho válido. O MSXML é mais estrito e gera um erro informando que o esquema não é determinístico.
  
Veja a seguir alguns exemplos de esquemas não determinísticos. O primeiro lida com elementos opcionais. Esses casos geralmente surgem dos conversores XDR para XSD devido às diferenças nas cardinalidades padrão nas duas linguagens de esquema. O primeiro caso a ser considerado é um elemento opcional declarado com **xsd: Choice** e **xsd: Sequence** Elements. Elementos opcionais declarados em um elemento **xsd: Sequence** normalmente validam adequadamente, contanto que você não tenha elementos com o mesmo nome mais de uma vez, com apenas elementos opcionais entre. Por exemplo: 
  
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

Olhando para este fragmento, você pode ver por que ele é inválido: há dois `<aNode>` elementos antes do `<anotherNode>` elemento, quando somente um é permitido. 
  
Agora, suponha que você tenha a seguinte instância XML para validar:
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

O desafio é determinar se essa instância é válida. Você tem dois `<aNode>` elementos, onde somente um é permitido ou você tem um `<aNode>` elemento onde ele é permitido e outro onde ele é permitido? O esquema não é determinístico, pois não há como saber. 
  
Da mesma forma, elementos opcionais declarados em um elemento **xsd: Choice** normalmente são problemáticos. No exemplo simplificado a seguir, não há como determinar se a escolha ocorreu uma vez com o elemento opcional não estar lá ou se nunca ocorreu. 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

A prática questionável final está usando um elemento **xsd: any** sem uma definição de namespace, como `<xsd:any namespace="##other"/>` in, após um elemento **xsd: Sequence** . Essa construção é especialmente problemática quando segue um elemento opcional. Se você revisitar o exemplo anterior e alterar apenas o último nó para um elemento **xsd: any** , poderá ver que todos os argumentos anteriores sobre não-determinantes ainda se aplicam, da seguinte maneira: 
  
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

Os esquemas XSD normalmente não realizam qualquer validação de tipo até você validar um documento de instância real. Uma exceção é quando você tem uma enumeração em seu esquema. Nesse caso, o esquema valida os valores de enumeração em relação aos tipos de enumeração para garantir que eles sejam valores de nó apropriados. Estes são dois exemplos:
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

Este esquema é inválido porque "onze horas" não é um valor válido para um elemento do tipo **xsd: time**.
  
Este é um exemplo mais complexo:
  
```XML
<xsd:simpleType name="concession"> 
    <xsd:restriction base="xsd:NMTOKEN"> 
        <xsd:enumeration value="GummyBears"/> 
        <xsd:enumeration value="SnowCaps"/> 
        <xsd:enumeration value="M&Ms"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

Para entender por que esse exemplo é inválido, você deve entender como o tipo **xsd: NMTOKEN** é definido. A especificação de tipos de dados W3C define o tipo **NMTOKEN** da seguinte maneira: "a NMTOKEN (token de nome) é qualquer mistura de caracteres de nome." 
  
Se você investigar mais, você descobrirá que ' & ' não é um caractere de nome válido e, portanto, "M&Ms" não valida como um tipo **NMTOKEN** . 
  
## <a name="empty-sequence-or-choice-elements"></a>Elementos de opção ou sequência vazia

O MSXML às vezes gera erros sobre declarações de esquema que contêm elementos **xsd: Choice** ou **xsd: Sequence** vazios, conforme mostrado no exemplo a seguir. 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

Remover a marca `<xsd:choice />` vazia deve resolver esse problema. 
  
## <a name="regular-expressions"></a>Expressões Regulares

O MSXML 5,0 pode ter problemas para validar padrões de expressão regular ao carregar. As expressões regulares podem ser complicadas e você deve ter cuidado ao usá-las. Cada analisador XSD parece ter idiomas de expressão regular flexíveis; ou seja, eles implementam os elementos da linguagem de expressão regular do XSD oficial, de outras linguagens de expressão regular. Se o designer de formulários do InfoPath tiver problemas para analisar uma expressão regular, os dados de exemplo que o InfoPath gerar poderão ser inválidos ou não serão gerados. Isso é aceitável no tempo de design, porque o InfoPath usa apenas dados de exemplo para formatação. No enTanto, se você usar uma expressão regular que o MSXML não oferece suporte, o InfoPath não poderá validar um valor em relação a ele quando um usuário estiver preenchendo um formulário. [Esquema XML parte 0: o primer segunda edição](https://www.w3.org/TR/xmlschema-0/)descreve o que é suportado em expressões regulares XSD. Para obter mais informações sobre expressões regulares de XSD e expressões regulares de nível 1 Unicode, consulte [expressões regulares Unicode](https://www.unicode.org/reports/tr18/) . 
  
## <a name="targetnamespace-attribute-issues"></a>Problemas de atributo targetNamespace

XSD é interessante, por padrão, que o atributo **targetNamespace** se refere apenas às declarações de nível superior, embora você possa definir `attributeFormDefault=qualified` e `elementFormDefault=qualified` substituir esse comportamento padrão. Por exemplo, suponha que você tenha o seguinte XSD. 
  
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

E isso, o documento de instância XML é semelhante ao exemplo a seguir.
  
```XML
<ns:root xmlns:ns="https://ns"> 
    <local/> 
</ns:root> 

```

As definições locais não exigem o namespace de destino porque a qualificação está desativada por padrão. No enTanto, se você alterar a definição local para ser global, a referência deverá ser qualificada com o prefixo de namespace. Por exemplo, o esquema a seguir é inválido.
  
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

Este esquema é inválido porque "global" está no namespace "https://ns". O Simple ref = "global" não é reconhecido porque o namespace padrão não é "https://ns". Para corrigir isso, você deve adicionar um prefixo para o namespace de destino e usá-lo para todas as referências globais e os usos de tipo. O esquema corrigido é semelhante ao seguinte.
  
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

Se o esquema tiver o atributo **targetNamespace** especificado, verifique se todas as referências globais estão qualificadas com o prefixo de namespace correto. 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a>Codificação de instrução de processamento XML (Unicode vs. ANSIi)

XML suporta apenas conjuntos de caracteres Unicode. Portanto, você pode perder informações se salvar arquivos que usam caracteres ANSIi. No enTanto, salvar arquivos como UTF-16 pode ser excessivo para seu uso específico. Para reduzir o custo de implementação de um leitor XML, o autor XML deve indicar qual codificação eles estão usando na instrução de processamento XML de nível superior. Você pode reconhecer a seguinte instrução de processamento.
  
```XML
xml version="1.0" encoding="UTF-8"
```

Essa marca de instrução de processamento especifica que a codificação do arquivo é UTF-8. Você deve garantir que a codificação do arquivo é a mesma que a codificação indicada na marca de instrução de processamento. Você pode determinar a codificação examinando os bytes do arquivo e procurando as marcas de ordem do byte Unicode. Mas há uma maneira mais fácil. Se você tiver problemas ao abrir um esquema XSD, especifique a codificação como "UTF-8", abra-o em um editor de texto, como o bloco de notas, e salve o arquivo usando a codificação UTF-8 (o bloco de notas fornece a lista suspensa de **codificação** na caixa de diálogo **salvar como** ). Se você ainda tiver problemas para abrir o arquivo, ele não será um problema de codificação. 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a>Atributo maxOccurs dentro do elemento xsd: ALL

Devido à forma como não determina o fato de que não é definido na recomendação de esquema XML, o único valor válido para o atributo **maxOccurs** de um elemento **xsd: Element** dentro de um elemento **xsd: ALL** é 1. Por exemplo, o seguinte é válido. 
  
```XML
<xsd:all> 
    <xsd:element name="x" minOccurs="0"/> 
    <xsd:element name="docs" minOccurs="0"/> 
</xsd:all> 

```

No enTanto, este exemplo não é válido.
  
```XML
<xsd:all>     
    <xsd:element name="x" minOccurs="0" maxOccurs="unbounded"/> 
    <xsd:element name="docs" minOccurs="0" maxOccurs="unbounded"/> 
</xsd:all> 

```

Este exemplo é inválido porque o sistema de validação não pode determinar se duas ocorrências de `<x/>` MAP à declaração única ou à declaração e outra definição inválida. Ao longo das mesmas linhas, não é possível ter dois elementos com o mesmo nome `<xsd:all>` em uma marca. 
  
Este exemplo também é interessante, pois permite que você tenha qualquer número de `<x/>` nós `<docs/>` e dentro de um elemento contido em qualquer ordem. Embora esse construtor seja inválido, há uma solução alternativa. Usando o elemento **xsd: Choice** , você pode obter o mesmo resultado, conforme demonstrado no exemplo a seguir. 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a>Como editar ou criar um XSD para o InfoPath

Os dois exemplos nas seções a seguir mostram como editar ou criar um esquema para produzir resultados específicos no InfoPath.
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a>Permitindo que elementos definidos pelo usuário sejam inseridos no painel de tarefas campos

Para permitir que os elementos definidos pelo usuário apareçam em um elemento pai no painel de tarefas **campos** , você deve inserir um elemento **xsd: any** no elemento pai. Para permitir que os elementos definidos pelo usuário sejam inseridos dentro `<your_node_name>` , a declaração XSD deve se parecer com o seguinte. 
  
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

Se você também quiser permitir atributos definidos pelo usuário, você deve adicionar `<xsd:anyAttribute namespace="##any | ##other"/>` à declaração do elemento. 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a>Permitindo que elementos de Rich Text sejam vinculados nos modos de design e edição do InfoPath

Se você quiser declarar um elemento que possa ser associado a um controle de **caixa de Rich Text** , ele deverá ter o seguinte formato, que inclui o elemento **xsd: any** que tenha um atributo namespace definido como "https://www.w3.org/1999/xhtml", conforme mostrado no exemplo a seguir. 
  
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

Aproveitando o suporte do InfoPath para criar soluções de formulário XML baseadas em arquivos de esquema XML criados externamente (. xsd), você pode criar um modelo de formulário que funciona com um esquema padrão da indústria ou com um esquema personalizado criado por sua empresa ou departamento. Usando as informações deste artigo, você pode criar arquivos de esquema XSD personalizados que são compatíveis com o InfoPath e pode solucionar problemas comuns que você pode encontrar ao carregar arquivos XSD criados externamente no ambiente de design do InfoPath.
  
## <a name="see-also"></a>Confira também

- [Esquema XML do W3C](https://www.w3.org/XML/Schema)
- [Primedor de esquema XML W3C](https://www.w3.org/TR/xmlschema-0/)
- [Referência de estruturas de esquema XML do W3C](https://www.xml.com/pub/a/2000/11/29/schemas/structuresref.html)
- [Referência de tipos de esquema W3C XML](https://www.xml.com/pub/a/2000/11/29/schemas/dataref.html)
- [Tutorial de esquema XML](https://www.w3schools.com/xml/schema_intro.asp)
- [Centro de desenvolvimento XML](https://msdn.microsoft.com/xml/default.aspx)

