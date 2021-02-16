---
title: Estrutura de fluxo FieldDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 98584e450bb820dbce05b0f8d2c6d15551586130
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334892"
---
# <a name="fielddefinition-stream-structure"></a>Estrutura de fluxo FieldDefinition

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma estrutura de fluxo FieldDefinition contém a definição de campo de um campo definido pelo usuário ou um conjunto de configurações de vinculação de dados para um campo integrado.
  
Você poderá manipular programaticamente uma estrutura de fluxo FieldDefinition se a estrutura contiver a definição de campo de um campo definido pelo usuário. Você não deve tentar criar ou modificar programaticamente uma estrutura FieldDefinition se a estrutura contiver configurações para um campo integrado. Você deve usar o Microsoft Outlook Forms Designer para manter essas configurações para campos integrados.
  
> [!NOTE]
> O Outlook dá suporte a dois formatos de definições de campo: PropDefV1 e PropDefV2. O formato PropDefV1 das definições de campo contém os seguintes elementos de dados: Flags, VT, DispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI e ErrorANSI. O formato PropDefV2 contém os mesmos elementos e os elementos InternalType e SkipBlocks. 
>
> O Outlook não mantém uma versão Unicode para os elementos de dados FormulaANSI, ValidationRuleANSI e ValidationTextANSI no formato de definição de campo PropDefV2. Se esses elementos contêm caracteres não ASCII, esses caracteres podem ser interpretados inconsistentemente dependendo da página de código ANSI do computador no qual o Outlook está sendo executado. Portanto, você deve usar somente valores de cadeia de caracteres que consistam inteiramente de caracteres ASCII para esses elementos de dados. 
  
Os elementos de dados nesse fluxo são armazenados em ordem de byte little-endian, imediatamente após uns aos outros na ordem especificada abaixo.
  
- Sinalizadores: DWORD (4 bytes), uma combinação de zero ou mais sinalizadores cujos valores e significados estão listados na tabela a seguir.
    
    |**Nome do sinalizador**|**Valor**|**Descrição**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |A estrutura FieldDefinition contém uma definição de um campo definido pelo usuário.  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Para um controle de formulário vinculado a esse campo, a caixa de seleção de **um** valor é necessária para esse campo está selecionada na guia **Validação** da **caixa** de diálogo Propriedades.  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |Para um controle de formulário vinculado a esse campo, a caixa de seleção Incluir este campo para impressão e Salvar **como** está selecionada na guia **Validação** da **caixa** de diálogo Propriedades.  <br/> |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |Para um controle de formulário vinculado a  esse campo, a  caixa de seleção Calcular essa fórmula automaticamente é selecionada na guia Valor da caixa **de** diálogo Propriedades.  <br/> |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |Este é um campo do tipo **Combinação** e tem os campos de Junção e os fragmentos de texto uns com os outros **selecionados** na caixa de diálogo Campo de Fórmula **de** Combinação.  <br/> |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |Esse campo é do tipo **Combinação** e tem a opção Mostrando apenas o primeiro campo não **vazio,** ignorando as opções subsequentes selecionadas na caixa de diálogo Campo de Fórmula **de** Combinação.  <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |Esse sinalizador não é usado pelo Outlook, mas é incluído para todas as definições de campo definidas pelo usuário.  <br/> |
   
- VT: WORD (2 bytes), o tipo de dados do campo, que é uma constante da enumeração [VARENUM.](https://msdn.microsoft.com/library/system.runtime.interopservices.varenum.aspx) 
    
- DispId: DWORD (4 bytes), o identificador de expedição do campo. Para um campo definido pelo usuário, o valor é 0.
    
- NmidNameLength: WORD (2 bytes), o número de elementos na matriz NmidName.
    
- NmidName: uma matriz de WCHAR. Para uma definição de campo definida pelo usuário, esta é a representação Unicode (UTF-16) do nome do campo. A contagem dessa matriz é igual a NmidNameLength.
    
- NameANSI: uma [estrutura de fluxo PackedAnsiString.](packedansistring-stream-structure.md) Esta é a representação ANSI do nome do campo. 
    
- FormulaANSI: uma estrutura de fluxo PackedAnsiString. Esta é uma representação ANSI da fórmula de cálculo do campo. Ele é mostrado na seção **Valor Inicial**  da guia **Valor** da caixa de diálogo Propriedades de um controle de formulário vinculado a esse campo. 
    
- ValidationRuleANSI: uma estrutura de fluxo PackedAnsiString. Esta é uma representação ANSI da fórmula de validação do campo. Ela é mostrada na caixa de texto **da**  Fórmula de Validação na guia **Validação** da caixa de diálogo Propriedades de um controle de formulário vinculado a esse campo. 
    
- ValidationTextANSI: uma estrutura de fluxo PackedAnsiString. Esta é uma representação ANSI do texto de falha de validação do campo. Ela será mostrada na caixa de texto Exibir esta  mensagem se  a validação falhar na guia Validação da caixa de diálogo Propriedades de um controle de formulário vinculado a esse campo.  
    
- ErrorANSI: uma estrutura de fluxo PackedAnsiString. O Outlook não usa esse elemento; você deve definir esse elemento como uma cadeia de caracteres vazia.
    
- InternalType: DWORD (4 bytes), o tipo interno do campo. Esse elemento de dados só estará presente se o formato de definição de campo for PropDefV2. O tipo interno é um dos seguintes valores, cada um  deles corresponde a um tipo na caixa de diálogo Novo Campo para campos definidos pelo usuário. 
    
    |**Nome do tipo interno**|**Valor**|**Tipo correspondente na **caixa de diálogo Novo** Campo**|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1   <br/> |**Número** <br/> |
    |iTypePercent  <br/> |2   <br/> |**Percent** <br/> |
    |Moeda  <br/> |3   <br/> |**Currency** <br/> |
    |iTypeBool  <br/> |4   <br/> |**Sim/Não** <br/> |
    |iTypeDateTime  <br/> |5   <br/> |**Data/Hora** <br/> |
    |iTypeDuration  <br/> |6   <br/> |**Duration** <br/> |
    |iTypeCombination  <br/> |7   <br/> |**Combination**, with the **Showing only the first non-empty field, ignoring subsequent ones** option selected in the Combination Formula **Field** dialog box.  <br/> |
    |iTypeFormula  <br/> |8   <br/> |**Fórmula** <br/> |
    |iTypeResult  <br/> |9   <br/> |Esse tipo não é usado para campos definidos pelo usuário.  <br/> |
    |iTypeVariant  <br/> |10   <br/> |Esse tipo não é usado para campos definidos pelo usuário.  <br/> |
    |iTypeFloatResult  <br/> |11  <br/> |Esse tipo não é usado para campos definidos pelo usuário.  <br/> |
    |iTypeConcat  <br/> |12   <br/> |**Combination**, with the **Joining fields and any text fragments with each other** option selected in the **Combination Formula Field** dialog box.  <br/> |
    |iTypeKeywords  <br/> |13   <br/> |**Palavra-chave** <br/> |
    |iTypeInteger  <br/> |14   <br/> |**Integer** <br/> |
   
- SkipBlocks: uma série de uma ou mais [estruturas de fluxo SkipBlock.](skipblock-stream-structure.md) Esse elemento de dados só estará presente se o formato de definição de campo for PropDefV2. Se o formato de definição de campo for PropDefV2, a série deve conter pelo menos uma estrutura SkipBlock, a estrutura SkipBlock que tem o elemento de dados Size igual a 0 e a série deve começar e terminar com essa estrutura SkipBlock. 
    
   O propósito de uma estrutura SkipBlock depende de sua posição relativa na série SkipBlocks. Se a definição de campo estiver no formato PropDefV2 e a primeira estrutura não for a estrutura de encerramento (o elemento de dados Size é maior que 0), o Outlook assumirá que a primeira estrutura SkipBlock especificará o nome do campo em Unicode (UTF-16). 
    
   > [!IMPORTANT]
   > Se o primeiro SkipBlock for a estrutura de encerramento, o elemento de dados NameANSI será usado para determinar o nome do campo. Se essa cadeia de caracteres contiver caracteres não ASCII, esses caracteres poderão ser interpretados inconsistentemente dependendo da página de código ANSI do computador no qual o Outlook está sendo executado. Para evitar essas inconsistências, certifique-se de sempre especificar o primeiro SkipBlock em definições de campo que você criar, pelo menos quando o nome do campo incluir caracteres não ASCII. 
  
   Se uma versão futura de um formato de definição de campo apresentar partes adicionais de dados no fluxo FieldDefinition, esses dados poderão ser armazenados como estruturas de fluxo SkipBlock adicionais na série SkipBlocks antes da terminação da estrutura SkipBlock que tem o elemento de dados Size igual a 0. As versões anteriores do Outlook podem ignorar com segurança essas estruturas SkipBlock extras até a estrutura SkipBlock de encerramento e ainda processar corretamente todos os blocos com suporte.
    
## <a name="see-also"></a>Confira também

- [Campos e itens do Outlook](outlook-items-and-fields.md)
- [Estruturas de fluxo](stream-structures.md)
- [Estrutura de fluxo PropertyDefinition](propertydefinition-stream-structure.md)

