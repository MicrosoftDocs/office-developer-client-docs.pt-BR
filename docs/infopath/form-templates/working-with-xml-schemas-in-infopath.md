---
title: Trabalhar com esquemas XML no InfoPath
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
# <a name="working-with-xml-schemas-in-infopath"></a>Trabalhar com esquemas XML no InfoPath

Um modelo de formulário que você criou com o Microsoft InfoPath usa um esquema XML (XSD) para executar estrutural e validação de dados em XML que é de entrada, editado, e a saída de um formulário do InfoPath. Cada modelo de formulário criado no InfoPath form designer contém pelo menos um arquivo de esquema XSD (. xsd) que é usado para validação em tempo de execução.
  
> [!NOTE]
> As informações contidas neste tópico se aplica a modelos de formulários projetados para uso no editor do InfoPath. Modelos de formulário compatíveis com navegador têm requisitos de esquema XSD mais restritas. Para obter mais informações, consulte a documentação sobre esquemas XML em modelos de formulário compatíveis com navegador disponíveis no MSDN. 
  
## <a name="using-externally-authored-xml-schemas"></a>Usando esquemas XML criados externamente

Para carregar um arquivo de esquema XSD que foi criado fora do InfoPath, siga estas etapas.
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a>Para criar um modelo de formulário baseado em um esquema externo

1. No Backstage, clique em **novo**, clique **XML ou esquema** em **Modelos de formulário avançado**e, em seguida, clique em **Criar este formulário**.
    
2. No **Assistente de fonte de dados**, especifique o arquivo de esquema XSD que você deseja usar e clique em **Avançar** e conclua as páginas restantes do assistente. 
    
## <a name="unsupported-xsd-constructs"></a>Construções XSD sem suporte

As seções a seguir descrevem construções XSD quais InfoPath não dá suporte em tempo de execução. Evite essas construções ao criar um modelo de formulário no designer de formulários do InfoPath.
  
## <a name="entity-and-entities-types"></a>ENTIDADE e tipos de ENTIDADES

Os tipos de **entidade** e **ENTIDADES** exigem uma definição de tipo de documento (DTD) para validação, que não dá suporte ao InfoPath. O InfoPath não permite a criação de um modelo de formulário com um esquema tal e exibe uma mensagem de erro que recomenda alterar o tipo de **entidade** para o tipo de **NCName** do qual deriva de **entidade** . 
  
> [!NOTE]
>  Se você cria manualmente um modelo de formulário do InfoPath fora do modo de design e ele usa um XSD que inclui os tipos de **entidade** e **ENTIDADES** , o modelo de formulário pode funcionar em tempo de execução se o arquivo de Template contiver o DTD necessário para esses tipos. 
  
## <a name="required-xsdany-element"></a>Obrigatório xsd: qualquer elemento

Uma ocorrência de um **xsd: qualquer** elemento curinga, ou seja, uma ocorrência de um **xsd: qualquer** elemento com um valor de atributo **minOccurs** maior do que zero ("obrigatório qualquer"), impede que o InfoPath forma determinista criando uma instância válida de Esse fragmento de esquema. InfoPath deve ser capaz de criar uma instância válida ao gerar um formulário que usa esse fragmento de esquema. Como parte da execução do **Assistente de fonte de dados**, esquemas com necessárias **xsd: qualquer** elementos exigem que você escolher qual elemento de esquema que você deseja usar no lugar required **xsd: qualquer** elemento. 
  
## <a name="elements-with-an-abstract-complex-type"></a>Elementos com um tipo complexo abstrato

Modo de design do InfoPath oferece suporte a criação de um modelo de formulário com base em esquemas que usam tipos complexos abstratos. Por exemplo, se um elemento chamado `shippingAddress` tem um tipo complexo abstrato denominado `address` que tem duas derivações, `USAddress` e `CanadianAddress`, InfoPath trata qualquer instância de `shippingAddress` como uma opção entre `shippingAddress` com tipo `USAddress` e `shippingAddress` com tipo `CanadianAddress` . Neste exemplo, se os esquemas fornecidos não contenham nenhum tipos que derivam do endereço, em seguida, InfoPath solicitações de um esquema adicional que atende a esse requisito. 
  
## <a name="xsd-constructs-with-reduced-functionality"></a>Construções XSD com funcionalidade reduzida

As seções a seguir descrevem construções XSD que reduziram funcionalidade quando usado para criar um modelo de formulário no designer de formulários do InfoPath.
  
## <a name="substitution-groups"></a>Grupos de substituição

Todos os membros do grupo de substituição aparecem no painel de tarefas **campos** . InfoPath representa as possibilidades de substituição como uma opção de todos os grupos de substituição (incluindo o elemento determinantes, se não for abstrata). Se não houver nenhuma grupos de substituição para um elemento abstrato, InfoPath solicita que você forneça um esquema que contém pelo menos um elemento que é um grupo de substituição. 
  
## <a name="unbounded-choice-elements"></a>Elementos de opção não vinculados

O fragmento de esquema a seguir mostra um elemento de escolha não vinculado:
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

InfoPath exibe os elementos de escolha de repetição como escolhas no painel de tarefas de **campos** de repetição. Não há um controle de **Grupo de escolha de repetição** que você pode usar para representar a lista heterogênea definida pelo elemento de escolha de repetição em XSD. 
  
## <a name="repeating-sequence"></a>Sequência de repetição

O fragmento de esquema a seguir mostra uma sequência de repetição:
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

Desde que a repetição sequência contiver um elemento necessário, o InfoPath carrega a XSD sem modificá-lo e permite associar controles de seção de repetição à sequência de repetição.
  
## <a name="choice-of-model-groups"></a>Escolha dos grupos de modelo

O fragmento de esquema a seguir mostra o elemento de opção que contém vários grupos de modelo:
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

Modo de design do InfoPath oferece suporte a tais construções XSD sem exigir qualquer modificação pelo criador do formulário. Enquanto o InfoPath não modifica o significado do esquema, ele simplifica a construção de opção acima em uma única opção no painel de tarefas **campos** do recolhido equivalente. 
  
## <a name="optional-sibling-with-same-qualified-name"></a>Irmão opcional com mesmo nome qualificado

O fragmento de esquema a seguir mostra um irmão opcional com mesmo nome qualificado (`QName`):
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

As expressões **XPath** para esses nós podem ser complexas, porque cada instância XML possível deve ser contabilizada no designer de formulários do InfoPath. InfoPath não expõe partes do esquema para o qual talvez tenha dificuldade para criar associações de **XPath** corretas. Avisos aparecem sobre as partes do esquema que serão ignoradas. 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a>Construções XSD com significado especial no InfoPath

As seções a seguir descrevem construções XSD que têm um significado especial quando usado na criação de um modelo de formulário no modo de design. Estas seções descrevem como você pode usar as construções no seu esquema para habilitar determinados comportamentos.
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a>Adicionando novos campos de elemento e grupos com o painel de tarefas de campos

Você pode construir o esquema para que você possa usar o painel de tarefas **campos** para adicionar novos campos de elemento e grupos a um elemento em tempo de design. Para fazer isso, você declarar um elemento no seu esquema com um opcional, não acoplados **xsd: qualquer** elemento que especifica o atributo de namespace com o **# # any** curinga. Em seguida, no modo de design, você pode usar o painel de tarefas **campos** para adicionar novos campos de elemento e grupos a esse elemento. Por exemplo, você pode adicionar novo conteúdo para o elemento a seguir: 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a>Adicionando novos campos de atributo com os campos de painel de tarefas

Da mesma forma como no caso de elemento, você pode declarar um atributo com um elemento **anyAttribute** que tem o atributo do namespace especificado como o **# # any** curinga. Em tempo de design, você pode usar o painel de tarefas **campos** para adicionar novo conteúdo para que esse atributo de esquema. 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a>Armazenando assinaturas XML na fonte de dados

Para habilitar usuários assinar digitalmente um formulário em tempo de execução, o esquema da fonte de dados deve declarar um elemento chamado assinatura para armazenar as informações de assinaturas de XML (assinatura digital) que são criadas quando um usuário se conecta o formulário. Você tornar esta declaração usando o **xsd: qualquer** elemento com o atributo do namespace especificado como o namespace de assinaturas XML com um caractere curinga, da seguinte maneira: "http://www.w3c.org/2000/09/xmldsig#" 
  
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

## <a name="binding-a-field-to-a-rich-text-box-control"></a>Associando um campo a um controle de caixa de Rich Text

 Controles de **Caixa de Rich Text** no InfoPath gerarem genérico XHTML; Consequentemente, seu esquema deve especificar que qualquer número de texto e nós XHTML é válido no XML da instância do formulário. É possível conseguir essa especificação com a construção XSD a seguir: 
  
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
> InfoPath nunca modifica o conteúdo do arquivo do esquema (. xsd), mas ela pode interpretar logicamente um subconjunto dela para fins de design. O arquivo de esquema é sempre tocado dentro do modelo de formulário em tempo de design e tempo de execução. 
  
## <a name="debugging-common-xsd-errors"></a>Depuração de erros comuns de XSD

Se você carregar arquivos XSD externamente criados para criar modelos de formulário no designer de formulários do InfoPath, você pode receber um dos dois tipos de mensagens de erro: MSXML mensagens de erro ou mensagens de erro do InfoPath. Mensagens de erro do MSXML aparecem na seção de **detalhes** de uma caixa de diálogo de mensagem de erro do InfoPath, e eles sempre comecem com uma referência para o nome ou o caminho do arquivo de esquema que está gerando o erro. Algumas construções de esquema XSD válidas não são suportadas pelo InfoPath; Estas são abordadas na seção constrói de XSD sem suporte. As seções a seguir descrevem alguns erros comuns que podem causar esquemas Falha ao carregar com êxito no InfoPath. 
  
## <a name="the-xsd-namespace-declaration"></a>A declaração de Namespace XSD

Semelhante ao todos os padrões W3C, esquemas XML (XSD) passou por um processo de revisão longos em seu caminho para se tornar uma recomendação. Havia muitas rascunhos de trabalho e, consequentemente, muitos arquivos XSD foram gravados com base nos seguintes evoluindo padrões. Durante esse processo, a Microsoft criou uma linguagem de esquema proprietárias chamada XML-Data Reduced (XDR) que foi incluído no MSXML 3.0. Começando com a versão do MSXML 4.0, o Microsoft XML Core Services oferece suporte a recomendação completa da XSD. Muitos programas para a criação de esquemas não aguardou XSD para se tornar uma recomendação completa. Versões mais antigas desses programas podem produzir arquivos XSD desatualizados que a infra-estrutura do MSXML 5.0, do qual o InfoPath depende, não oferece suporte.
  
Para garantir que um arquivo XSD suporta a recomendação de XSD completa, ele deve conter a seguinte declaração de namespace XML no \<esquema\> tag:
  
```XML
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
```

Da mesma forma que todas as declarações de namespace XML, o prefixo XML (no caso 'xsd') pode ser qualquer cadeia de caracteres de prefixo válido. Alguns prefixos comuns, talvez você veja prática são 'xsd', 'x,' e ' (sem prefixo). MSXML geralmente relata um erro sobre a raiz não está sendo definida corretamente se esta declaração de namespace está ausente.
  
## <a name="importing-and-including-schemas"></a>Importando e incluindo esquemas

Esquemas XSD são extensíveis e importe e incluir outros esquemas. Em geral, você deve importar um esquema se o esquema especificado no atributo **targetNamespace** difere do esquema atual. Você deve incluí-lo se o esquema especificado no atributo **targetNamespace** é o mesmo que o esquema atual. 
  
A semântica de importação e incluindo esquemas é:
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

Se o atributo **schemaLocation** estiver faltando (como acontece com alguns conversores), e depois MSXML gerará um erro, porque não é possível encontrar o arquivo. Se você receber esse erro, também Certifique-se de que o recurso ou o local especificado no atributo schemaLocation está acessível pelos usuários do modelo de formulário. Obviamente, erros ocorrem se o atributo **schemaLocation** faz referência a um servidor ou o diretório que está inoperante ou inexistente, ou se os usuários não têm permissões de acesso. Além disso, certifique-se de examinar todos os esquemas importados e incluídos para certificar-se de que eles são válidos. 
  
> [!NOTE]
> Erros causados por problemas com o atributo **schemaLocation** são um problema quando o InfoPath primeiro importa os esquemas; ou seja, quando você inicia a criação de um formulário baseado em um esquema existente. Depois disso, o InfoPath funciona com versões em cache dos arquivos de esquema que são armazenados no modelo de formulário. 
  
Um atributo de namespace vazio é permitido durante a importação de um esquema, se esse esquema não especificar um atributo **targetNamespace** . Em geral, o espaço para nome na página Importar deve corresponder o **targetNamespace** especificado no esquema de que você importar. 
  
## <a name="nondeterministic-schemas"></a>Esquemas não determinísticas

A infraestrutura de MSXML 5.0 que depende do InfoPath confiável pode detectar e geram erros para alertá-lo aos esquemas não determinísticas, mas a mensagem de erro resultante não fornece um número de linha para dizer que parte do esquema é elevar o erro. Esta seção discute porque é importante para os arquivos de esquema XSD ser determinantes e o que significa ser não determinístico. Ele também mostra alguns erros comuns para evitar.
  
Esquemas XSD existirem com o objetivo de validar semântica de estrutura e o tipo de dados XML. Para realizar essa tarefa, o sistema de validação (no caso, MSXML 5.0) deve mapear nós XML para declarações de XSD. Sem esse mapeamento, o sistema de validação não é possível realizar suas tarefas. Se um mapeamento pode ser garantido, o esquema é determinante. Se houver uma única instância XML que torna impossível esse mapeamento, o esquema é não determinístico.
  
O esquema de exemplo a seguir é não determinístico:
  
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

Para ilustrar o motivo pelo qual este segmento XSD é não determinístico, pressupõem que você tem o seguinte fragmento XML que você deseja validar com esse esquema:
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

Neste fragmento de XML, não é criptografado se o * \<file_path\> * elemento é o nó obrigatório da primeira parte da declaração de opção ou uma opcional da segunda parte da declaração de opção. Essa distinção é importante pelos seguintes motivos: 
  
1. Se o fragmento XML é validado em relação a primeira parte da declaração de opção, o XML é válido em relação ao esquema.
    
2. Se o fragmento XML é validado em relação a segunda parte da declaração de opção, então o esquema não é válido, pois required \<URI\> nó está ausente. 
    
Alguns sistemas de validação XSD err em direção Validando contra este esquema porque não há um caminho válido. MSXML é mais restrito e gera um erro informando que o esquema é não determinístico.
  
O que segue é alguns exemplos de mais de esquemas não determinísticas. O primeiro lida com elementos opcionais. Nesses casos frequentemente provenientes de XDR conversores XSD devido às diferenças na cardinalities padrão nos idiomas dois esquema. O primeiro caso a serem considerados é opcionais elementos declarados com elementos **xsd:choice** e **xsd:sequence** . Elementos opcionais declarados em um elemento **xsd:sequence** geralmente validar corretamente, desde que você não possui elementos com o mesmo nome mais de uma vez, com apenas os elementos opcionais entre si. Por exemplo: 
  
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

Para entender por que esse segmento do esquema é não determinístico, pressupõem que você tem o inválido fragmento XML a seguir:
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
    <anotherNode/> 
</container> 

```

Olhando esse fragmento, você pode ver por que ele é inválido: há dois `<aNode>` elementos antes do `<anotherNode>` elemento, quando somente um é permitido. 
  
Agora, suponha que você tenha a seguinte instância XML para validar:
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

O desafio é para determinar se esta instância é válida. Você tem dois `<aNode>` elementos onde somente um é permitido ou tem um `<aNode>` elemento onde ele é permitido e outro onde é permitido? O esquema é não determinístico porque não é possível saber. 
  
Da mesma forma, os elementos opcionais declarados em um elemento **xsd:choice** são geralmente problemáticos. No exemplo a seguir simplificado, há um meio para determinar se a opção ocorreu depois com o elemento opcional não estar ao vivo ou se ele nunca ocorreu nisso. 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

A prática questionável final está usando um **xsd: qualquer** elemento sem uma definição de namespace, como em `<xsd:any namespace="##other"/>` , após um elemento **xsd:sequence** . Essa construção é especialmente problemática quando vier um elemento opcional. Se você rever o exemplo anterior e altera o último nó para um **xsd: qualquer** elemento, você pode ver que todos os argumentos anteriores sobre nondeterminism ainda se aplicam, da seguinte maneira: 
  
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

Esquemas XSD geralmente não realize qualquer tipo de validação até que você valida um documento de instância real. Uma exceção é quando você tem uma enumeração no seu esquema. Nesse caso, o esquema valida os valores de enumeração contra os tipos de enumeração para garantir que eles são valores de nó apropriado. Aqui estão dois exemplos:
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

Este esquema é inválido, como "11 horas" não é um valor válido para um elemento do tipo **xsd: time**.
  
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

Para entender por que neste exemplo é inválido, é preciso entender como o tipo **xsd:NMTOKEN** é definido. A especificação de tipos de dados W3C define o tipo **NMTOKEN** da seguinte maneira: "É qualquer mistura de caracteres de nome de um NMTOKEN (token nome)." 
  
Se você investigar melhor, você descobre que ' e ' não é um nome válido de caractere e, portanto, "M & Ms" não valida como um tipo **NMTOKEN** . 
  
## <a name="empty-sequence-or-choice-elements"></a>Sequência vazia ou elementos de opção

Às vezes, o MSXML gera erros sobre declarações de esquema que contêm vazio **xsd:choice** ou **xsd:sequence** elementos, conforme mostrado no exemplo a seguir. 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

Removendo a esvaziar `<xsd:choice />` marca deve resolver esse problema. 
  
## <a name="regular-expressions"></a>Expressões Regulares

MSXML 5.0 pode ter problemas ao validar os padrões de expressão regular no carregamento. Expressões regulares podem ser complexas, e você deve tomar cuidado quando você estiver usando-los. Cada analisador XSD parece ter idiomas de expressão regular flexível; ou seja, implemente a linguagem de expressão regular XSD oficial mais elementos de outros idiomas de expressão regular. Se o designer de formulários do InfoPath tiver problemas ao analisar uma expressão regular, os dados de amostra que InfoPath gera seja inválidos ou não podem ser gerados em todos os. Isso é aceitável em tempo de design, porque o InfoPath usa apenas os dados de amostra para formatação. No entanto, se você usar uma expressão regular que não oferece suporte a MSXML, InfoPath não é possível validar um valor em relação a ele quando um usuário preenche um formulário. [Parte do esquema XML 0: Primer Second Edition](http://www.w3.org/TR/xmlschema-0/)descreve o que é suportado em expressões regulares de XSD. Para obter mais informações sobre expressões regulares de XSD e expressões regulares de nível 1 de Unicode, consulte [Expressões regulares Unicode](http://www.unicode.org/reports/tr18/) . 
  
## <a name="targetnamespace-attribute-issues"></a>targetNamespace problemas de atributo

XSD é interessante em que, por padrão, o atributo **targetNamespace** refere-se ao somente as declarações de nível superior, embora você possa definir `attributeFormDefault=qualified` e `elementFormDefault=qualified` para substituir esse comportamento padrão. Como exemplo, suponha que você tenha a seguir XSD. 
  
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

E que, seu XML instância documento semelhante ao exemplo a seguir.
  
```XML
<ns:root xmlns:ns="http://ns"> 
    <local/> 
</ns:root> 

```

Definições de locais não exigem o namespace de destino porque qualificação está desativada por padrão. No entanto, se você alterar sua definição de local para ser global, sua referência deve ser qualificada com o prefixo do namespace. Por exemplo, o esquema a seguir é inválido.
  
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

Este esquema é inválido porque é "global" no namespace "http://ns". O simple ref = "global" não seja reconhecida porque o namespace padrão não é "http://ns". Para corrigir esse problema, você deve adicionar um prefixo para o namespace de destino e usá-la para todas as referências globais e digite usos. O esquema correto é semelhante ao seguinte.
  
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

Se seu esquema tiver o atributo **targetNamespace** especificado, certifique-se de que todas as referências globais estão qualificadas com o prefixo de namespace correto. 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a>A instrução codificação (Unicode versus ANSII) de processamento de XML

XML suporta apenas os conjuntos de caracteres Unicode. Portanto, você poderá perder informações se salvar arquivos que usam ANSII caracteres. No entanto, o salvamento de arquivos como UTF-16 pode ser excessivo para seu uso específico. Para reduzir o custo de implementação de um leitor de XML, o autor XML deve estado qual codificação estão usando no nível superior XML instrução de processamento. Você pode reconhecer a seguinte instrução de processamento.
  
```XML
xml version="1.0" encoding="UTF-8"
```

Nesta marca de instrução de processamento Especifica que a codificação do arquivo é UTF-8. Certifique-se de que a codificação do arquivo é o mesmo conforme a codificação mencionado na marca de instrução de processamento. Você pode determinar a codificação olhando os bytes do arquivo e procurando pelas marcas de ordem de byte Unicode. Mas não há uma maneira mais fácil. Se você tiver problemas ao abrir um esquema XSD, especificar a codificação como "UTF-8", abri-lo em um editor de texto como o bloco de notas e salve o arquivo usando a codificação UTF-8 (o bloco de notas fornece a lista suspensa **codificação** na caixa de diálogo **Salvar como** ). Se você ainda tiver problemas ao abrir o arquivo, ele não é um problema de codificação. 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a>maxOccurs atributo dentro do elemento xsd:all

Devido à maneira nondeterminism definida na recomendação de esquema XML, o único valor válido para o atributo **maxOccurs** de um elemento **xsd: element** dentro de um elemento **xsd:all** é 1. Por exemplo, o seguinte é válido. 
  
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

Este exemplo é inválido porque o sistema de validação não pode determinar se dois ocorrências da `<x/>` mapa à declaração única ou para a declaração e outra definição inválida. Sob a mesma perspectiva, você não pode ter dois elementos do mesmo nome em uma `<xsd:all>` marca. 
  
Este exemplo também é interessante porque ela permite que você tenha qualquer número de `<x/>` e `<docs/>` nós dentro de um elemento contendo em qualquer ordem. Embora essa construção for inválida, há uma solução alternativa. Usando o elemento **xsd:choice** , você pode obter o mesmo resultado, conforme demonstrado no exemplo a seguir. 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a>Como editar ou criar um XSD do InfoPath

Os dois exemplos nas seções a seguir mostram como editar ou criar um esquema para produzir resultados específicos no InfoPath.
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a>Permitindo que os elementos definidos pelo usuário a ser inserido no painel de tarefas campos

Para permitir que os elementos definida pelo usuário seja exibido em um elemento pai no painel de tarefas **campos** , você deve inserir um **xsd: qualquer** elemento sob o elemento pai. Para permitir que os elementos definidos pelo usuário a ser inserido dentro `<your_node_name>` , a declaração de XSD deve se parecer com o seguinte. 
  
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

Se você também deseja permitir atributos definidos pelo usuário, você deve adicionar `<xsd:anyAttribute namespace="##any | ##other"/>` na declaração de elemento. 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a>Permitindo que os elementos de texto Rich deve ser vinculada no Design do InfoPath e editar modos

Se você deseja declarar um elemento que pode ser vinculado a um controle de **Caixa de Rich Text** , então ela deve ter o seguinte formato, que inclui o **xsd: qualquer** elemento que possui um atributo de namespace definido como "http://www.w3.org/1999/xhtml" conforme mostrado no exemplo a seguir. 
  
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

## <a name="conclusion"></a>Conclusão

Ao aproveitar o suporte do InfoPath para criar soluções de formulário XML que se baseiam em arquivos de esquema XML (. xsd) externamente criados, você pode criar um modelo de formulário que funciona com um esquema de padrão do setor ou um esquema personalizado criado por sua empresa ou organização. Usando as informações neste artigo, você pode criar arquivos de esquema XSD personalizados que são compatíveis com o InfoPath, e você pode solucionar problemas comuns que podem ocorrer quando você carregar arquivos XSD externamente criados no ambiente de design do InfoPath.
  
## <a name="see-also"></a>Confira também

- [Esquema XML do W3C](http://www.w3.org/XML/Schema)
- [Cartilha de esquema XML W3C](http://www.w3.org/TR/xmlschema-0/)
- [Referência de estruturas de esquema do W3C XML](http://www.xml.com/pub/a/2000/11/29/schemas/structuresref.mdl)
- [Referência de tipos de dados de esquema do W3C XML](http://www.xml.com/pub/a/2000/11/29/schemas/dataref.mdl)
- [Tutorial do esquema XML](http://www.w3schools.com/schema/default.asp)
- [Central de desenvolvedores de XML](http://msdn.microsoft.com/en-us/xml/default.aspx)

