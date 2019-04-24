---
title: Estruturas de fluxo de campos de pasta
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96051bd2b62fd7c0e908a1018aac0225e44986be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336887"
---
# <a name="folder-fields-stream-structures"></a>Estruturas de fluxo de campos de pasta

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A propriedade [PidTagUserFields](pidtaguserfields-canonical-property.md) de uma mensagem contém um fluxo binário, FolderUserFields, que contém as definições de campo definidas pelo usuário da pasta. Este tópico descreve as estruturas de fluxo para as definições de campo definidas pelo usuário da pasta. 

Uma estrutura de fluxo FolderUserFields consiste em uma estrutura FolderUserFieldsA ou uma estrutura FolderUserFieldsA seguida de uma estrutura FolderUserFieldsW.
  
Os elementos de dados neste fluxo são armazenados imediatamente após um ao outro na seguinte ordem especificada:
  
- **FolderUserFieldsAnsi**: uma estrutura de fluxo de FolderUserFieldsA.
    
- **FolderUserFieldsUnicode** (opcional): uma estrutura de fluxo do FolderUserFieldsW.
    
A presença de FolderUserFieldsUnicode é detectada pelo tamanho total do FolderUserFields que é maior do que o comprimento de FolderUserFieldsAnsi.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi é usado para compatibilidade com versões mais antigas, não-Unicode, de clientes MAPI, portanto, se FolderUserFieldsUnicode estiver presente, o conteúdo de FolderUserFieldsAnsi será ignorado. Para evitar a possível perda de dados na conversão ANSI, ao criar um fluxo de FolderUserFields sempre inclua a parte FolderUserFieldsW. 
  
## <a name="folderuserfieldsa-stream-structure"></a>Estrutura de fluxo FolderUserFieldsA

Uma estrutura de fluxo FolderUserFieldsA é uma matriz de estruturas de fluxo do FolderFieldDefinitionA que contêm definições para todos os campos definidos pelo usuário em uma pasta do Outlook, a menos que seja substituída pela parte FolderUserFieldsW da estrutura FolderUserFields.
  
Os elementos de dados neste fluxo são armazenados em uma ordem de byte little-endian, imediatamente após o outro na seguinte ordem especificada:
  
- **FieldDefinitionCount**: DWORD (4 bytes), o número de definições de campo neste fluxo. Esta é a contagem dos elementos na matriz **FieldDefinitions** .
    
- **FieldDefinitions**: uma matriz de estruturas de fluxo do FolderFieldDefinitionA. A contagem dessa matriz é igual ao elemento de dados **FieldDefinitionCount** .
    
A menos que esse FolderUserFieldsA seja substituído pela parte FolderUserFieldsW da estrutura FolderUserFields, a matriz **FieldDefinitions** deve ser "terminada em nulo", tendo o campo Common. FieldType do último elemento FolderFieldDefinitionA igual a para o ftNull.
  
## <a name="folderuserfieldsw-stream-structure"></a>Estrutura de fluxo FolderUserFieldsW

Uma estrutura de fluxo do FolderUserFieldsW é uma matriz de estruturas de fluxo do FolderFieldDefinitionW que contêm definições para todos os campos definidos pelo usuário em uma pasta do Outlook.
  
Os elementos de dados neste fluxo são armazenados em uma ordem de byte little-endian, imediatamente após o outro na seguinte ordem especificada:
  
- **FieldDefinitionCount**: DWORD (4 bytes), o número de definições de campo neste fluxo. Esta é a contagem dos elementos na matriz **FieldDefinitions** .
    
- **FieldDefinitions**: uma matriz de estruturas de fluxo do FolderFieldDefinitionW. A contagem dessa matriz é igual ao elemento de dados **FieldDefinitionCount** .
    
A matriz **FieldDefinitions** deve ser "terminada em nulo" com o último campo. FieldType do elemento FolderFieldDefinitionW igual a ftNull.
  
## <a name="folderfielddefinitiona-stream-structure"></a>Estrutura de fluxo FolderFieldDefinitionA

Uma estrutura de fluxo FolderFieldDefinitionA contém uma definição de um campo definido pelo usuário com o nome do campo armazenado em ANSI.
  
Os elementos de dados neste fluxo são armazenados em uma ordem de byte little-endian, imediatamente após o outro na seguinte ordem especificada:
  
- **FieldType**: FldType (4 bytes), o tipo desse campo.
    
- **FieldNameLength**: Word (2 bytes), o número de elementos na matriz **FieldName** .
    
- **FieldName**: uma matriz de Char. Esta é a representação de página de código ANSI CP_ACP do nome do campo. A contagem dessa matriz é igual a **FieldNameLength**. O nome do campo deve satisfazer as restrições no parâmetro Name conforme especificado no método [UserProperties. Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Por motivos de compatibilidade herdada, o Outlook pode ser capaz de lidar com alguns valores de **FieldName** que não satisfaçam essas restrições, mas esses casos não são cobertos por este tópico. 
  
- **Comum**: uma estrutura de fluxo do FolderFieldDefinitionCommon.
    
## <a name="folderfielddefinitionw-stream-structure"></a>Estrutura de fluxo FolderFieldDefinitionW

Uma estrutura de fluxo FolderFieldDefinitionW contém uma definição de um campo definido pelo usuário com o nome do campo armazenado em Unicode.
  
Os elementos de dados neste fluxo são armazenados em uma ordem de byte little-endian, imediatamente após o outro na seguinte ordem especificada:
  
- **FieldType**: FldType (4 bytes), o tipo desse campo.
    
- **FieldNameLength**: Word (2 bytes), o número de elementos na matriz **FieldName** .
    
- **FieldName**: uma matriz de WCHAR. Esta é a representação Unicode (UTF-16) do nome do campo. A contagem dessa matriz é igual a **FieldNameLength**. O nome do campo deve satisfazer as restrições no parâmetro Name conforme especificado no método [UserProperties. Add](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Por motivos de compatibilidade herdada, o Outlook pode ser capaz de lidar com alguns valores de **FieldName** que não satisfaçam essas restrições, mas esses casos não são cobertos por este tópico. 
  
- **Comum**: uma estrutura de fluxo do FolderFieldDefinitionCommon.
    
## <a name="fldtype-enumeration"></a>Enumeração FldType

Os valores de enumeração **FldType** estão listados na tabela a seguir. 
  
|Nome|Valor|Significado|
|:-----|:-----|:-----|
|ftNull  <br/> |0x0  <br/> |Este tipo de campo é usado para anular uma matriz de definições de campos.  <br/> |
|ftString  <br/> |0x1  <br/> |Texto  <br/> |
|ftInteger  <br/> |0x3  <br/> |Inteiro  <br/> |
|ftTime  <br/> |0x5  <br/> |Data/Hora  <br/> |
|ftBoolean  <br/> |0x6  <br/> |Sim/Não  <br/> |
|ftDuration  <br/> |0x7  <br/> |Duração  <br/> |
|ftMultiString  <br/> |0xB  <br/> |Palavras-chave  <br/> |
|ftFloat  <br/> |0xC  <br/> |Número ou porcentagem  <br/> |
|ftCurrency  <br/> |0xE  <br/> |Moeda  <br/> |
|ftCalc  <br/> |0x12  <br/> |Fórmula  <br/> |
|ftSwitch  <br/> |0x13  <br/> |Combinação de tipo mostrando apenas o primeiro campo não vazio, ignorando os itens subsequentes.  <br/> |
|ftConcat  <br/> |0x17  <br/> |Combinação do tipo associando campos e qualquer fragmento de texto.  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>Estrutura de fluxo FolderFieldDefinitionCommon

Uma estrutura de fluxo FolderFieldDefinitionCommon contém os dados de uma definição de campo definido pelo usuário que é comum para um FolderFieldDefinitionA e um FolderFieldDefinitionW.
  
Os elementos de dados neste fluxo são armazenados em uma ordem de byte little-endian, imediatamente após o outro na seguinte ordem especificada:
  
- **PropSetGuid**: GUID (16 bytes), o GUID do conjunto de propriedades do nome da propriedade MAPI correspondente do campo de pasta. O valor deste campo deve ser igual a PS_PUBLIC_STRINGS, a menos que o tipo de campo seja **ftNone** nesse caso, o valor deste campo deve ser igual a GUID_NULL. 
    
   > [!NOTE]
   > Por motivos de compatibilidade herdada, o Outlook pode ser capaz de lidar com alguns valores de **PropSetGuid** que não satisfaçam essa restrição, mas esses casos não são cobertos por este tópico. 
  
- **fcapm**: DWORD (4 bytes), uma combinação de zero ou mais sinalizadores os valores dos quais e significados estão listados na tabela a seguir. Sinalizadores com o mesmo valor têm significados dependentes do tipo do campo, ou seja, o valor de FldType.
    
    |Nome do sinalizador|Valor|Significado|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |O campo é editável.  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |O campo é classificável.  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |O campo é agrupável.  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |O campo pode conter várias linhas de texto.  <br/> |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |Este campo do tipo ftFloat é um campo de porcentagem.  <br/> |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |Este campo do tipo ftTime é um campo de hora somente data.  <br/> |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |Para este campo do tipo ftInteger, nenhuma unidade é permitida no formato de exibição; por exemplo, tais formatos como "computador-640 K..." Não são permitidas.  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |O campo pode ser editado no item: especificamente para formulários personalizados.  <br/> |
   
- **dwString**: DWORD (4 bytes). Consulte a primeira anotação a seguir.
    
- **dwBitmap**: DWORD (4 bytes). Consulte a primeira anotação a seguir.
    
- **dwDisplay**: DWORD (4 bytes). Consulte a primeira anotação a seguir.
    
- **iFmt**: int (4 bytes). Para os tipos de campo que têm a caixa de combinação "formato:" nas caixas de diálogo "novo campo", "editar campo" e "Propriedades do campo", o índice com base em 0 do formato selecionado na caixa de combinação. Para os tipos de campo sem essa caixa de combinação, deve ser 0. O valor do campo junto com o tipo de campo determina exclusivamente os valores dos campos **dwString**, **dwBitmap**e **DwDisplay** , consulte a primeira nota a seguir.
    
- **wszFormulaLength**: Word (2 bytes), o número de elementos na matriz **wszFormulaLength** .
    
- **wszFormulaLength**: uma matriz de WCHAR. Esta é a representação Unicode (UTF-16) da cadeia de caracteres de fórmula do campo em seu formato padrão. Consulte a segunda nota para obter a descrição dos formatos padrão e de interface do usuário da fórmula de um campo. A contagem dessa matriz é igual a **wszFormulaLength**. A cadeia de caracteres de fórmula deve ser uma cadeia de caracteres vazia, a menos que o tipo de campo seja **ftCalc**, **ftSwitch** ou **ftConcat**.
    
> [!NOTE]
> Embora os valores de **dwString**, **dwBitmap**e **dwDisplay** sejam determinados exclusivamente com base no valor de **FldType** e no valor de **iFmt** , que são redundantes, seus valores corretos ainda são necessários para o correto processamento da definição de campo pelo Outlook. Não há uma descrição simples do algoritmo que realiza essa determinação. 
> 
> Portanto, para descobrir quais valores de **dwString**, **dwBitmap**e **dwDisplay** correspondem a um determinado valor **FldType** e **iFmt** , execute um teste criando um campo definido pelo usuário desse tipo e com esse formato selecionado na caixa de combinação **Formatar** , supondo sua aplicabilidade, inspecione o fluxo **FolderUserFields** resultante que o Outlook cria para esse campo definido pelo usuário. 
  
A fórmula do campo em seu formato de interface do usuário é editada na caixa de texto **fórmula** das caixas de diálogo **novo**campo, **Editar campo**e **Propriedades de campo** para o campo definido pelo usuário. O algoritmo para converter uma fórmula do formato de interface do usuário para o formato padrão depende do tipo de campo, conforme descrito no seguinte: 
- Para campos dos tipos **ftCalc** e **ftSwitch**, o formato padrão para campos internos, quais propriedades MAPI correspondentes não são propriedades nomeadas da cadeia de caracteres de\_tipo MNID, são obtidas pela substituição de fragmentos de nome `[<field_name>]` de campo, ou seja, com fragmentos `[_<field_dispid_decimal>]`. 

  Por exemplo, se o formato de interface do usuário de uma fórmula para um campo da **fórmula**de tipo, que é **ftCalc**, com o idioma da interface do usuário `[Business Phone] & [My custom field]`do Office `My custom field` em inglês, é, onde é o nome de um campo definido pelo usuário, o formato padrão de tal fórmula seria `[_14856] & [My custom field]`.

- Para campos do tipo **ftConcat**, o formato padrão é obtido executando o seguinte:

  1. Truncar espaços em branco à esquerda e à direita. 
  2. Analise a fórmula em uma sequência de fragmentos dos dois tipos a seguir: 
     - Um nome de campo em colchetes, ou seja, `[<field_name>]`. 
     - Uma subcadeia de caracteres que não contém colchetes.   
      Certifique-se de que não há dois fragmentos do segundo tipo adjacentes na sequência. Se a fórmula não pode ser analisada dessa forma, ela é considerada inválida. 
  3. Execute a mesma substituição de fragmentos do primeiro tipo para os campos **ftCalc** e **ftSwitch** . 
  4. Para cada fragmento do segundo tipo, escape todos os caracteres de aspas duplas ("" "), se houver, com dois caracteres consecutivos de aspas duplas e coloque-o entre aspas duplas. 
  5. Inserir uma cadeia de caracteres`&`de e comercial () entre cada par de fragmentos adjacentes.
 
  Por exemplo, usando o idioma da interface do usuário do Office inglês dos EUA, se o formato da interface do usuário de uma fórmula `text1 [Business Phone] "text2" [My custom field]`para um `My custom field` campo do tipo **ftConcat** for, onde é o nome de um campo definido pelo usuário, o formato `""text1" & [_14856] & """text2""" & [My custom field]"`padrão para tal fórmula seria. 
  
## <a name="see-also"></a>Confira também

- [Exemplo de fluxo FolderUserFields](folderuserfields-stream-sample.md)
- [Adicionar uma definição para um novo campo definido pelo usuário](how-to-add-a-definition-for-a-new-user-defined-field.md)

