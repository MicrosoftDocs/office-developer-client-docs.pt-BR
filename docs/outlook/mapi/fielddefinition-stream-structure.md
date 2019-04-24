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
  
Uma estrutura de fluxo FieldDefinition contém a definição de campo de um campo definido pelo usuário ou um conjunto de configurações de associação de dados para um campo interno.
  
Você pode manipular programaticamente uma estrutura de fluxo do FieldDefinition se a estrutura contiver a definição de campo de um campo definido pelo usuário. Você não deve tentar criar ou modificar programaticamente uma estrutura FieldDefinition se a estrutura contiver configurações para um campo interno. Você deve usar o designer de formulários do Microsoft Outlook para manter essas configurações para campos internos.
  
> [!NOTE]
> O Outlook oferece suporte a dois formatos de definições de campo: PropDefV1 e PropDefV2. O formato PropDefV1 das definições de campo contém os seguintes elementos de dados: flags, VT, DispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI e ErrorANSI. O formato PropDefV2 contém os mesmos elementos e os elementos InternalType e SkipBlocks. 
>
> O Outlook não mantém uma versão Unicode para os elementos de dados FormulaANSI, ValidationRuleANSI e ValidationTextANSI no formato de definição de campo PropDefV2. Se esses elementos contiverem caracteres não-ASCII, esses caracteres poderão ser interpretados de forma inconsistente, dependendo da página de código ANSI do computador em que o Outlook está sendo executado. Portanto, você deve usar somente valores de cadeia de caracteres que consistam inteiramente de caracteres ASCII para esses elementos de dados. 
  
Os elementos de dados neste fluxo são armazenados em uma ordem de byte little-endian, imediatamente após o outro na ordem especificada abaixo.
  
- Flags: DWORD (4 bytes), uma combinação de zero ou mais sinalizadores cujos valores e significados estão listados na tabela a seguir.
    
    |**Nome do sinalizador**|**Valor**|**Descrição**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |A estrutura FieldDefinition contém uma definição de um campo definido pelo usuário.  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Para um controle de formulário acoplado a esse campo, a caixa de seleção de **um valor é necessária para este campo** é selecionado na guia **validação** da caixa de diálogo **Propriedades** .  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |Para um controle de formulário acoplado a esse campo, a caixa de seleção **incluir este campo para impressão e salvar como** está selecionada na guia **validação** da caixa de diálogo **Propriedades** .  <br/> |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |Para um controle de formulário acoplado a esse campo, a caixa de seleção para **calcular esta fórmula automaticamente** está selecionada na guia **valor** da caixa de diálogo **Propriedades** .  <br/> |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |Este é um campo de **combinação** de tipos e tem os **campos de ingresso e fragmentos de texto com cada** opção selecionada na caixa de diálogo de **campo de fórmula de combinação** .  <br/> |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |Este campo é de **combinação** de tipo e tem **apenas o primeiro campo não vazio, ignorando** a opção de opções subsequentes selecionada na caixa de diálogo de **campo de fórmula de combinação** .  <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |Esse sinalizador não é usado pelo Outlook, mas está incluído em todas as definições de campo definidas pelo usuário.  <br/> |
   
- VT: WORD (2 bytes), o tipo de dados do campo, que é uma constante da enumeração [VarEnum](https://msdn.microsoft.com/library/system.runtime.interopservices.varenum.aspx) . 
    
- DispId: DWORD (4 bytes), o identificador de despacho do campo. Para um campo definido pelo usuário, o valor é 0.
    
- NmidNameLength: WORD (2 bytes), o número de elementos na matriz NmidName.
    
- NmidName: uma matriz de WCHAR. Para uma definição de campo definido pelo usuário, esta é a representação Unicode (UTF-16) do nome do campo. A contagem dessa matriz é igual a NmidNameLength.
    
- NameANSI: uma estrutura de fluxo de [PackedAnsiString](packedansistring-stream-structure.md) . Esta é a representação ANSI do nome do campo. 
    
- FormulaANSI: uma estrutura de fluxo de PackedAnsiString. Esta é uma representação ANSI da fórmula de cálculo para o campo. Ela é mostrada na seção **valor inicial** da guia **valor** da caixa de diálogo **Propriedades** de um controle de formulário acoplado a esse campo. 
    
- ValidationRuleANSI: uma estrutura de fluxo de PackedAnsiString. Esta é uma representação ANSI da fórmula de validação do campo. Ela é mostrada na caixa de texto para **fórmula de validação** na guia **validação** da caixa de diálogo **Propriedades** de um controle de formulário acoplado a esse campo. 
    
- ValidationTextANSI: uma estrutura de fluxo de PackedAnsiString. Esta é uma representação ANSI do texto de falha de validação do campo. Ela é mostrada na caixa de texto para **exibir esta mensagem se a validação falhar** na guia **validação** da caixa de diálogo **Propriedades** de um controle de formulário acoplado a esse campo. 
    
- ErrorANSI: uma estrutura de fluxo de PackedAnsiString. O Outlook não usa esse elemento; Você deve definir esse elemento como uma cadeia de caracteres vazia.
    
- InternalType: DWORD (4 bytes), o tipo interno do campo. Este elemento de dados só estará presente se o formato de definição de campo for PropDefV2. O tipo interno é um dos valores a seguir, cada um deles corresponde a um tipo na caixa de diálogo **novo campo** para campos definidos pelo usuário. 
    
    |**Nome do tipo interno**|**Valor**|**Tipo correspondente na caixa de diálogo **novo campo****|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |,0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1  <br/> |**Número** <br/> |
    |iTypePercent  <br/> |duas  <br/> |**Percent** <br/> |
    |Moeda  <br/> |3D  <br/> |**Currency** <br/> |
    |iTypeBool  <br/> |quatro  <br/> |**Sim/Não** <br/> |
    |iTypeDateTime  <br/> |0,5  <br/> |**Data/Hora** <br/> |
    |iTypeDuration  <br/> |6  <br/> |**Duration** <br/> |
    |iTypeCombination  <br/> |178  <br/> |**Combinação**, com o **mostrando apenas o primeiro campo não vazio, ignorando** a opção de opções subsequentes selecionada na caixa de diálogo de **campo de fórmula de combinação** .  <br/> |
    |iTypeFormula  <br/> |8  <br/> |**Fórmula** <br/> |
    |iTypeResult  <br/> |241  <br/> |Este tipo não é usado para campos definidos pelo usuário.  <br/> |
    |iTypeVariant  <br/> |254  <br/> |Este tipo não é usado para campos definidos pelo usuário.  <br/> |
    |iTypeFloatResult  <br/> |11  <br/> |Este tipo não é usado para campos definidos pelo usuário.  <br/> |
    |iTypeConcat  <br/> |3,6  <br/> |**Combinação**, com os **campos unindo e todos os fragmentos de texto com cada** opção selecionada na caixa de diálogo **combinação de campos de fórmula** .  <br/> |
    |iTypeKeywords  <br/> |Treze  <br/> |**Chaves** <br/> |
    |iTypeInteger  <br/> |14  <br/> |**Integer** <br/> |
   
- SkipBlocks: uma série de uma ou mais estruturas de fluxo do [SkipBlock](skipblock-stream-structure.md) . Este elemento de dados só estará presente se o formato de definição de campo for PropDefV2. Se o formato de definição de campo for PropDefV2, a série deve conter pelo menos uma estrutura SkipBlock, a estrutura SkipBlock que tem o elemento de dados de tamanho igual a 0 e a série deve começar e terminar com esta estrutura SkipBlock. 
    
   A finalidade de uma estrutura SkipBlock depende de sua posição relativa na série SkipBlocks. Se a definição do campo estiver no formato PropDefV2 e a primeira estrutura não for a estrutura de terminação (o elemento de dados size for maior que 0), o Outlook presumirá que a primeira estrutura do SkipBlock especifica o nome do campo em Unicode (UTF-16). 
    
   > [!IMPORTANT]
   > Se o primeiro SkipBlock é a estrutura de terminação, o elemento de dados NameANSI é usado para determinar o nome do campo. Se essa cadeia de caracteres contiver caracteres não-ASCII, esses caracteres poderão ser interpretados de forma inconsistente, dependendo da página de código ANSI do computador em que o Outlook está sendo executado. Para evitar essas inconsistências, certifique-se de que você sempre especifique o primeiro SkipBlock nas definições de campo que você criou, pelo menos quando o nome do campo inclui caracteres não-ASCII. 
  
   Se uma versão futura de um formato de definição de campo apresentar partes adicionais de dados no fluxo do FieldDefinition, esses dados podem ser armazenados como estruturas de fluxo do SkipBlock adicionais na série SkipBlocks antes da estrutura SkipBlock de finalização que tem o Elemento de tamanho de dados igual a 0. As versões anteriores do Outlook podem ignorar com segurança essas estruturas SkipBlock extras até a estrutura de SkipBlock de finalização e ainda processar corretamente todos os blocos que oferecem suporte a eles.
    
## <a name="see-also"></a>Confira também

- [Campos e itens do Outlook](outlook-items-and-fields.md)
- [Estruturas de fluxo](stream-structures.md)
- [Estrutura de fluxo PropertyDefinition](propertydefinition-stream-structure.md)

