---
title: Estrutura de fluxo de FieldDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 93acdbc8-381f-45d5-be6c-0cad066269fe
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 775dc1b5fdcf40867f67fbab25879bd97de24f4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766538"
---
# <a name="fielddefinition-stream-structure"></a>Estrutura de fluxo de FieldDefinition

**Aplica-se a**: Outlook 
  
Uma estrutura de fluxo de FieldDefinition contém a definição de campo de um campo definido pelo usuário ou um conjunto de definições de ligação de dados de um campo interna.
  
Você pode manipular programaticamente uma estrutura de fluxo de FieldDefinition se a estrutura contém a definição de campo de um campo definido pelo usuário. Você não deve tentar programaticamente criar ou modificar uma estrutura de FieldDefinition se a estrutura contém configurações de um campo interna. Você deve usar o Designer de formulários do Microsoft Outlook para manter tais configurações para campos internos.
  
> [!NOTE]
> O Outlook oferece suporte a dois formatos das definições de campo: PropDefV1 e PropDefV2. O formato PropDefV1 das definições de campo contém os seguintes elementos de dados: sinalizadores, VT, DispId, NmidNameLength, NmidName, NameANSI, FormulaANSI, ValidationRuleANSI, ValidationTextANSI e ErrorANSI. O formato PropDefV2 contém os mesmos elementos e os elementos InternalType e SkipBlocks. 
>
> O Outlook não mantém uma versão Unicode para os elementos de dados FormulaANSI, ValidationRuleANSI e ValidationTextANSI no formato de definição de campo PropDefV2. Se esses elementos contiverem caracteres não-ASCII, esses caracteres podem ser interpretados de forma inconsistente, dependendo da página de código ANSI do computador no qual o Outlook estiver sendo executado. Portanto, você deve usar somente os valores de cadeia de caracteres que consistem inteiramente em caracteres ASCII para esses elementos de dados. 
  
Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após a outra na ordem especificada abaixo.
  
- Sinalizadores: DWORD (4 bytes), uma combinação de zero ou mais sinalizadores cujos valores e significados estão listados na tabela a seguir.
    
    |**Nome do sinalizador**|**Valor**|**Descrição**|
    |:-----|:-----|:-----|
    |PDO_IS_CUSTOM  <br/> |0x00000001  <br/> |A estrutura FieldDefinition contém uma definição de um campo definido pelo usuário.  <br/> |
    |PDO_REQUIRED  <br/> |0x00000002  <br/> |Para um controle de formulário acoplado a esse campo, a caixa de seleção **é necessário um valor para esse campo** é selecionada na guia **validação** da caixa de diálogo **Propriedades** .  <br/> |
    |PDO_PRINT_SAVEAS  <br/> |0x00000004  <br/> |Para um controle de formulário acoplado a esse campo, a caixa de seleção **incluir este campo para impressão e salvar como** está selecionado na guia **validação** da caixa de diálogo **Propriedades** .  <br/> |
    |PDO_CALC_AUTO  <br/> |0x00000008  <br/> |Para um controle de formulário acoplado a esse campo, a caixa de seleção para **Calcular esta fórmula automaticamente** está selecionada na guia **valor** da caixa de diálogo **Propriedades** .  <br/> |
    |PDO_FT_CONCAT  <br/> |0x00000010  <br/> |Este é um campo de tipo de **combinação** e tem a opção de **Unindo campos e qualquer fragmentos de texto uns com os outros** selecionada na sua caixa de diálogo **Campo de fórmula de combinação** .  <br/> |
    |PDO_FT_SWITCH  <br/> |0x00000020  <br/> |Este campo é do tipo **combinação** e selecionou a opção **mostrando apenas o primeiro campo não vazio, ignorando os demais** na caixa de diálogo **Campo de fórmula de combinação** .  <br/> |
    |PDO_PRINT_SAVEAS_DEF  <br/> |0x00000040  <br/> |Esse sinalizador não é usado pelo Outlook, mas é incluído para todas as definições de campo definido pelo usuário.  <br/> |
   
- VT: WORD (2 bytes), o tipo de dados do campo, que é uma constante da enumeração [VARENUM](http://msdn.microsoft.com/en-us/library/system.runtime.interopservices.varenum.aspx) . 
    
- DispId: DWORD (4 bytes), o identificador de distribuição do campo. Para um campo definido pelo usuário, o valor é 0.
    
- NmidNameLength: WORD (2 bytes), o número de elementos na matriz NmidName.
    
- NmidName: Uma matriz de WCHAR. Para uma definição de campo definido pelo usuário, essa é a representação Unicode (UTF-16) do nome do campo. A contagem dessa matriz é igual a NmidNameLength.
    
- NameANSI: Uma [PackedAnsiString](packedansistring-stream-structure.md) stream estrutura. Esta é a representação ANSI do nome do campo. 
    
- FormulaANSI: Uma PackedAnsiString stream estrutura. Esta é uma representação ANSI da fórmula de cálculo para o campo. Ele é mostrado na seção **Valor inicial** da guia **valor** da caixa de diálogo **Propriedades** de um controle de formulário acoplado a esse campo. 
    
- ValidationRuleANSI: Uma PackedAnsiString stream estrutura. Esta é uma representação ANSI da fórmula de validação do campo. Ele é mostrado na caixa de texto de **Fórmula de validação** na guia **validação** da caixa de diálogo **Propriedades** de um controle de formulário acoplado a esse campo. 
    
- ValidationTextANSI: Uma PackedAnsiString stream estrutura. Esta é uma representação ANSI do texto de falha de validação do campo. Ele é mostrado na caixa de texto para **Exibir esta mensagem se a validação falhar** na guia **validação** da caixa de diálogo **Propriedades** de um controle de formulário acoplado a esse campo. 
    
- ErrorANSI: Uma PackedAnsiString stream estrutura. O Outlook não usa esse elemento; Você deve definir esse elemento como uma sequência vazia.
    
- InternalType: DWORD (4 bytes), o tipo interno do campo. Este elemento de dados está presente apenas se o formato de definição de campo é PropDefV2. O tipo interno é um dos valores a seguir, cada um dos quais corresponde a um tipo na caixa de diálogo **Novo campo** para campos definidos pelo usuário. 
    
    |**Nome do tipo interno**|**Valor**|**Tipo correspondente na caixa de diálogo **Novo campo****|
    |:-----|:-----|:-----|
    |iTypeString  <br/> |0  <br/> |**Text** <br/> |
    |iTypeNumber  <br/> |1  <br/> |**Número** <br/> |
    |iTypePercent  <br/> |2  <br/> |**Percent** <br/> |
    |Moeda  <br/> |3  <br/> |**Moeda** <br/> |
    |iTypeBool  <br/> |4  <br/> |**Sim/Não** <br/> |
    |iTypeDateTime  <br/> |5  <br/> |**Data/hora** <br/> |
    |iTypeDuration  <br/> |6  <br/> |**Duração** <br/> |
    |iTypeCombination  <br/> |7  <br/> |**Combinação**, com a opção **mostrando apenas o primeiro campo não vazio, ignorando os demais** selecionada na caixa de diálogo **Campo de fórmula de combinação** .  <br/> |
    |iTypeFormula  <br/> |8  <br/> |**Formula** <br/> |
    |iTypeResult  <br/> |9  <br/> |Esse tipo não é usado para campos definidos pelo usuário.  <br/> |
    |iTypeVariant  <br/> |10  <br/> |Esse tipo não é usado para campos definidos pelo usuário.  <br/> |
    |iTypeFloatResult  <br/> |11  <br/> |Esse tipo não é usado para campos definidos pelo usuário.  <br/> |
    |iTypeConcat  <br/> |12  <br/> |**Combinação**, com a opção de **Unindo campos e qualquer fragmentos de texto uns com os outros** selecionada na caixa de diálogo **Campo de fórmula de combinação** .  <br/> |
    |iTypeKeywords  <br/> |13  <br/> |**Palavra-chave** <br/> |
    |iTypeInteger  <br/> |14  <br/> |**Integer** <br/> |
   
- SkipBlocks: Uma série de uma ou mais estruturas de fluxo de [SkipBlock](skipblock-stream-structure.md) . Este elemento de dados está presente apenas se o formato de definição de campo é PropDefV2. Se o formato de definição de campo for PropDefV2, a série deve conter pelo menos uma estrutura de SkipBlock, a estrutura de SkipBlock que tem o elemento de dados de tamanho igual a 0, e a série deve começar e terminar com essa estrutura SkipBlock. 
    
   A finalidade de uma estrutura SkipBlock depende de sua posição relativa na série SkipBlocks. Se a definição de campo está no formato PropDefV2 e a estrutura primeira não é a estrutura de encerramento (o elemento de dados de tamanho é maior que 0), o Outlook pressupõe que a estrutura de SkipBlock primeira Especifica o nome do campo em Unicode (UTF-16). 
    
   > [!IMPORTANT]
   > Se o primeiro SkipBlock é a estrutura de encerramento, o elemento de dados de NameANSI é usado para determinar o nome do campo. Se essa sequência contiver quaisquer caracteres não ASCII, esses caracteres podem ser interpretados de forma inconsistente, dependendo da página de código ANSI do computador no qual o Outlook estiver sendo executado. Para evitar essas inconsistências, certifique-se de que você especificar sempre o primeiro SkipBlock nas definições de campo que você criar, pelo menos quando o nome do campo inclui caracteres não ASCII. 
  
   Se uma versão futura do formato de uma definição de campo introduz adicionais partes de dados no stream FieldDefinition, esses dados podem ser armazenados como estruturas de fluxo de SkipBlock adicionais na série SkipBlocks antes da estrutura SkipBlock terminação que possui o Elemento de dados de tamanho igual a 0. Versões anteriores do Outlook podem ignorar com segurança essas estruturas SkipBlock extras até a estrutura de SkipBlock terminação e ainda corretamente processar todos os blocos que oferecem suporte a eles.
    
## <a name="see-also"></a>Confira também

- [Campos e itens do outlook](outlook-items-and-fields.md)
- [Estruturas de fluxo](stream-structures.md)
- [Estrutura de fluxo de PropertyDefinition](propertydefinition-stream-structure.md)

