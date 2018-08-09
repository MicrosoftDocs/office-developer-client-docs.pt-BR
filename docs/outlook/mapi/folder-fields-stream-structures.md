---
title: Estruturas de fluxo do campo de pastas
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: edbc9e6c-008c-4c13-9a0c-cb47ac0f3686
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d6724914896fe7c40e9a456785aa5c92b84532fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766573"
---
# <a name="folder-fields-stream-structures"></a>Estruturas de fluxo do campo de pastas

**Aplica-se a**: Outlook 
  
Propriedade de [PidTagUserFields](pidtaguserfields-canonical-property.md) da mensagem contém um fluxo binário, FolderUserFields, que contém as definições de campo definido pelo usuário da pasta. Este tópico descreve as estruturas de fluxo para definições de campo definido pelo usuário da pasta. 

Uma estrutura de fluxo de FolderUserFields consiste em uma estrutura de FolderUserFieldsA ou uma estrutura de FolderUserFieldsA seguido por uma estrutura FolderUserFieldsW.
  
Elementos este fluxo de dados são armazenados imediatamente após uns aos outros na seguinte ordem especificada:
  
- **FolderUserFieldsAnsi**: estrutura de fluxo de um FolderUserFieldsA.
    
- **FolderUserFieldsUnicode** (opcional): um FolderUserFieldsW stream estrutura.
    
A presença de FolderUserFieldsUnicode é detectada pelo comprimento total do FolderUserFields sendo maior que o comprimento de FolderUserFieldsAnsi.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi é usado para compatibilidade com mais antigo, não-Unicode, versões de clientes MAPI, portanto, se FolderUserFieldsUnicode estiver presente, o conteúdo de FolderUserFieldsAnsi é ignorado. Para evitar possíveis dados perda na conversão ANSI, ao criar um fluxo de FolderUserFields sempre incluir a parte de FolderUserFieldsW. 
  
## <a name="folderuserfieldsa-stream-structure"></a>Estrutura de fluxo de FolderUserFieldsA

Uma estrutura de fluxo de FolderUserFieldsA é uma matriz de estruturas de fluxo de FolderFieldDefinitionA que contém definições para todos os campos definidos pelo usuário em uma pasta do Outlook, a menos que substituída pela parte FolderUserFieldsW da estrutura FolderUserFields.
  
Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após uns aos outros na seguinte ordem especificada:
  
- **FieldDefinitionCount**: DWORD (4 bytes), o número de definições de campo neste fluxo. É a contagem de elementos na matriz **FieldDefinitions** .
    
- **FieldDefinitions**: uma matriz de FolderFieldDefinitionA stream estruturas. A contagem dessa matriz é igual ao elemento **FieldDefinitionCount** dados.
    
A menos que essa FolderUserFieldsA é substituído pela parte FolderUserFieldsW da estrutura FolderUserFields, a matriz de **FieldDefinitions** deve ser "terminada em nulo" fazendo com que o campo de Common.FieldType do elemento seu FolderFieldDefinitionA última igual para ftNull.
  
## <a name="folderuserfieldsw-stream-structure"></a>Estrutura de fluxo de FolderUserFieldsW

Uma estrutura de fluxo de FolderUserFieldsW é uma matriz de estruturas de fluxo de FolderFieldDefinitionW que contém definições para todos os campos definidos pelo usuário em uma pasta do Outlook.
  
Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após uns aos outros na seguinte ordem especificada:
  
- **FieldDefinitionCount**: DWORD (4 bytes), o número de definições de campo neste fluxo. É a contagem de elementos na matriz **FieldDefinitions** .
    
- **FieldDefinitions**: uma matriz de FolderFieldDefinitionW stream estruturas. A contagem dessa matriz é igual ao elemento **FieldDefinitionCount** dados.
    
A matriz **FieldDefinitions** deve ser "terminada em nulo" fazendo com que o campo de Common.FieldType do elemento seu FolderFieldDefinitionW última igual a ftNull.
  
## <a name="folderfielddefinitiona-stream-structure"></a>Estrutura de fluxo de FolderFieldDefinitionA

Uma estrutura de fluxo de FolderFieldDefinitionA contém uma definição de um campo definido pelo usuário com o nome de campo armazenado no ANSI.
  
Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após uns aos outros na seguinte ordem especificada:
  
- **FieldType**: FldType (4 bytes), o tipo deste campo.
    
- **FieldNameLength**: WORD (2 bytes), o número de elementos na matriz **FieldName** .
    
- **FieldName**: uma matriz de CHAR. Esta é a representação de página de código ANSI CP_ACP do nome do campo. A contagem dessa matriz é igual a **FieldNameLength**. O nome do campo deve satisfazer as restrições no parâmetro nome conforme especificado no método [UserProperties](http://msdn.microsoft.com/en-us/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Por motivos de compatibilidade herdado, Outlook pode ser capaz de manipular alguns valores de **FieldName** não atendem a essas restrições, porém nesses casos não são cobertos neste tópico. 
  
- **Comuns**: estrutura de fluxo de um FolderFieldDefinitionCommon.
    
## <a name="folderfielddefinitionw-stream-structure"></a>Estrutura de fluxo de FolderFieldDefinitionW

Uma estrutura de fluxo de FolderFieldDefinitionW contém uma definição de um campo definido pelo usuário com o nome do campo armazenado em Unicode.
  
Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após uns aos outros na seguinte ordem especificada:
  
- **FieldType**: FldType (4 bytes), o tipo deste campo.
    
- **FieldNameLength**: WORD (2 bytes), o número de elementos na matriz **FieldName** .
    
- **FieldName**: uma matriz de WCHAR. Esta é a representação Unicode (UTF-16) do nome do campo. A contagem dessa matriz é igual a **FieldNameLength**. O nome do campo deve satisfazer as restrições no parâmetro nome conforme especificado no método [UserProperties](http://msdn.microsoft.com/en-us/library/microsoft.office.interop.outlook.userproperties.add.aspx) . 
    
   > [!NOTE]
   > Por motivos de compatibilidade herdado, Outlook pode ser capaz de manipular alguns valores **FieldName** não atendem a essas restrições, mas nesses casos não são cobertos neste tópico. 
  
- **Comuns**: estrutura de fluxo de um FolderFieldDefinitionCommon.
    
## <a name="fldtype-enumeration"></a>Enumeração FldType

Valores de enumeração **FldType** estão listados na tabela a seguir. 
  
|Name|Value|Meaning|
|:-----|:-----|:-----|
|ftNull  <br/> |0x0  <br/> |Esse tipo de campo é usado para null-encerrar uma matriz das definições de campo.  <br/> |
|ftString  <br/> |0x1  <br/> |Texto  <br/> |
|ftInteger  <br/> |0x3  <br/> |Inteiro  <br/> |
|ftTime  <br/> |0x5  <br/> |Data/Hora  <br/> |
|ftBoolean  <br/> |0x6  <br/> |Sim/Não  <br/> |
|ftDuration  <br/> |0x7  <br/> |Duração  <br/> |
|ftMultiString  <br/> |0xB  <br/> |Keywords  <br/> |
|ftFloat  <br/> |0xC  <br/> |Número ou porcentagem  <br/> |
|ftCurrency  <br/> |0xE  <br/> |Moeda  <br/> |
|ftCalc  <br/> |0x12  <br/> |Fórmula  <br/> |
|ftSwitch  <br/> |0x13  <br/> |Combinação de tipo mostrando apenas o primeiro campo não vazias - ignorando os demais.  <br/> |
|ftConcat  <br/> |0x17  <br/> |Combinação de tipo Unindo campos e qualquer fragmento de texto uns aos outros.  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>Estrutura de fluxo de FolderFieldDefinitionCommon

Uma estrutura de fluxo de FolderFieldDefinitionCommon contém os dados de uma definição de campo definido pelo usuário que é comum para um FolderFieldDefinitionA e um FolderFieldDefinitionW.
  
Elementos este fluxo de dados são armazenados na ordem de bytes pouca-endian, imediatamente após uns aos outros na seguinte ordem especificada:
  
- **PropSetGuid**: GUID (16 bytes), a propriedade definida GUID do nome da propriedade MAPI correspondente do campo pasta. O valor desse campo deve ser igual a PS_PUBLIC_STRINGS, a menos que o tipo de campo é **ftNone** nesse caso, o valor desse campo deve ser igual a GUID_NULL. 
    
   > [!NOTE]
   > Por motivos de compatibilidade herdado, Outlook pode ser capaz de manipular alguns valores **PropSetGuid** não atendem a essa restrição, porém nesses casos não são cobertos neste tópico. 
  
- **fcapm**: DWORD (4 bytes), uma combinação de sinalizadores de zero ou mais valores de qual e significados estão listados na tabela a seguir. Sinalizadores com o mesmo valor tem significados dependentes do tipo de campo, ou seja, o valor FldType.
    
    |Nome do sinalizador|Value|Meaning|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |O campo é editável.  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |O campo pode ser classificado.  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |O campo é agrupável.  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |O campo pode conter várias linhas de texto.  <br/> |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |Este campo de ftFloat o tipo é um campo de porcentagem.  <br/> |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |Este campo de ftTime o tipo é um campo time somente Data.  <br/> |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |Para esse campo de ftInteger o tipo, nenhuma unidade é permitida no formato de exibição; Por exemplo formatos como "Computador - 640 k..." não são permitidos.  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |O campo pode ser editado no item: Este é especificamente para formulários personalizados.  <br/> |
   
- **dwString**: DWORD (4 bytes). Consulte a observação a seguir primeira.
    
- **dwBitmap**: DWORD (4 bytes). Consulte a observação a seguir primeira.
    
- **dwDisplay**: DWORD (4 bytes). Consulte a observação a seguir primeira.
    
- **iFmt**: INT (4 bytes). Para os tipos de campo que tenham o "formato:" dialogs de caixa de combinação na "Novo campo", "Editar campo" e "Propriedades de campo", o índice baseado em 0 do formato selecionado nessa caixa de combinação. Para os tipos de campo dessa caixa de combinação, isso deve ser de 0. O valor do campo em conjunto com o tipo de campo exclusivamente determina os valores do **dwString**, **dwBitmap**, e **dwDisplay** campos, consulte a observação a seguir primeira.
    
- **wszFormulaLength**: WORD (2 bytes), o número de elementos na matriz **wszFormulaLength** .
    
- **wszFormulaLength**: uma matriz de WCHAR. Esta é a representação Unicode (UTF-16) da cadeia de caracteres fórmula em seu formato padrão do campo. Consulte a observação a seguir segunda para a descrição do padrão e formatos de interface do usuário da fórmula de um campo. A contagem dessa matriz é igual a **wszFormulaLength**. A fórmula cadeia de caracteres deve ser uma cadeia de caracteres vazia, a menos que o tipo de campo é **ftCalc**, **ftSwitch** ou **ftConcat**.
    
> [!NOTE]
> Embora os valores de **dwString**, **dwBitmap**e **dwDisplay** exclusivamente são determinados com base no valor de **FldType** e o valor de **iFmt** , que são redundantes, seus valores corretos ainda são necessários para correto processamento de definição de campo pelo Outlook. Não há nenhuma descrição simple do algoritmo que está executando essa determinação. 
> 
> Portanto, para descobrir quais valores **dwString**, **dwBitmap**e **dwDisplay** correspondem a um determinado valor **FldType** e um valor de **iFmt** , realize um teste criando um campo definido pelo usuário desse tipo e com esse formato selecionado Na caixa de combinação **formato** , supondo que a sua capacidade de aplicação, inspecione o fluxo **FolderUserFields** resultante que o Outlook cria para esse campo definido pelo usuário. 
  
A fórmula do campo em seu formato de interface do usuário é editada na caixa de texto de **fórmula** do **Novo campo**, **Edite o campo**e caixas de diálogo **Propriedades do campo** para o campo definido pelo usuário. O algoritmo para converter uma fórmula do formato de interface do usuário para o formato padrão depende do tipo de campo, conforme descrito a seguir: 
- Para campos de tipos **ftCalc** e **ftSwitch**, o formato padrão para campos internos, as propriedades correspondentes do MAPI que não estão denominado propriedades do kind MNID\_cadeia de caracteres, é obtido substituindo fragmentos de nome de campo, ou seja `[<field_name>]` com fragmentos `[_<field_dispid_decimal>]`. 

  Por exemplo, se o formato de interface do usuário de uma fórmula de um campo do tipo **fórmula**, que é **ftCalc**, com o idioma da UI do Office sendo inglês dos Estados Unidos, é `[Business Phone] & [My custom field]`, onde `My custom field` é o nome de um campo definido pelo usuário, o formato padrão de tal uma fórmula seria `[_14856] & [My custom field]`.

- Para campos do tipo **ftConcat**, o formato padrão é obtido executando o seguinte:

  1. Truncar o espaço em branco à direita e à esquerda. 
  2. Analise a fórmula em uma sequência de fragmentos dos dois seguintes tipos: 
     - Um nome de campo entre colchetes, ou seja, `[<field_name>]`. 
     - Uma subcadeia de caracteres que não contêm quaisquer colchetes.   
      Garanta que nenhum dois fragmentos do segundo tipo são adjacentes na sequência. Se a fórmula não pode ser analisada dessa maneira, ele será considerado inválido. 
  3. Execute a mesma substituição para fragmentos do primeiro tipo às propriedades dos campos **ftCalc** e **ftSwitch** . 
  4. Para cada fragmento do segundo tipo, escape todas as aspas duplas ("" ") caracteres, se houver, com dois caracteres de aspas duplas consecutivas e coloque-o entre aspas duplas. 
  5. Inserir uma cadeia de caracteres de e comercial (`&`) entre cada par de fragmentos adjacentes.
 
  Por exemplo, usando o idioma da interface de usuário Office inglês dos Estados Unidos, se o formato de interface do usuário de uma fórmula de um campo do tipo **ftConcat** for `text1 [Business Phone] "text2" [My custom field]`, onde `My custom field` é o nome de um campo definido pelo usuário, o formato padrão para esta fórmula seria `""text1" & [_14856] & """text2""" & [My custom field]"`. 
  
## <a name="see-also"></a>Confira também

- [Exemplo de fluxo de FolderUserFields](folderuserfields-stream-sample.md)
- [Adicionar uma definição de um novo campo definido pelo usuário](how-to-add-a-definition-for-a-new-user-defined-field.md)

