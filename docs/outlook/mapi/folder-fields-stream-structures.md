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
  
A propriedade [PidTagUserFields](pidtaguserfields-canonical-property.md) de uma mensagem contém um fluxo binário, FolderUserFields, que contém as definições de campo definidas pelo usuário da pasta. Este tópico descreve as estruturas de fluxo para definições de campo definidas pelo usuário da pasta. 

Uma estrutura de fluxo FolderUserFields consiste em uma estrutura FolderUserFieldsA ou uma estrutura FolderUserFieldsA seguida por uma estrutura FolderUserFieldsW.
  
Os elementos de dados nesse fluxo são armazenados imediatamente após os outros na seguinte ordem especificada:
  
- **FolderUserFieldsAnsi**: uma estrutura de fluxo FolderUserFieldsA.
    
- **FolderUserFieldsUnicode** (opcional): uma estrutura de fluxo FolderUserFieldsW.
    
A presença de FolderUserFieldsUnicode é detectada pelo comprimento total de FolderUserFields sendo maior do que o comprimento de FolderUserFieldsAnsi.
  
> [!IMPORTANT]
> FolderUserFieldsAnsi é usada para compatibilidade com versões mais antigas e não Unicode de clientes MAPI, portanto, se FolderUserFieldsUnicode estiver presente, o conteúdo de FolderUserFieldsAnsi será ignorado. Para evitar possível perda de dados na conversão ANSI, ao criar um fluxo FolderUserFields sempre inclua a parte FolderUserFieldsW. 
  
## <a name="folderuserfieldsa-stream-structure"></a>Estrutura de Fluxo de FolderUserFieldsA

Uma estrutura de fluxo FolderUserFieldsA é uma matriz de estruturas de fluxo FolderFieldDefinitionA que contêm definições para todos os campos definidos pelo usuário em uma pasta do Outlook, a menos que seja substituído pela parte FolderUserFieldsW da estrutura FolderUserFields.
  
Os elementos de dados nesse fluxo são armazenados em ordem de byte little-endian, imediatamente após uns aos outros na seguinte ordem especificada:
  
- **FieldDefinitionCount**: DWORD (4 bytes), o número de definições de campo neste fluxo. Esta é a contagem de elementos na **matriz FieldDefinitions.**
    
- **FieldDefinitions**: uma matriz de estruturas de fluxo FolderFieldDefinitionA. A contagem dessa matriz é igual ao elemento de dados **FieldDefinitionCount.**
    
A menos que essa FolderUserFieldsA seja substituído pela parte FolderUserFieldsW da estrutura FolderUserFields, a matriz **FieldDefinitions** deverá ser "terminada em nulo" tendo seu último campo Common.FieldType do elemento FolderFieldDefinitionA igual a ftNull.
  
## <a name="folderuserfieldsw-stream-structure"></a>Estrutura de fluxo folderUserFieldsW

Uma estrutura de fluxo FolderUserFieldsW é uma matriz de estruturas de fluxo FolderFieldDefinitionW que contêm definições para todos os campos definidos pelo usuário em uma pasta do Outlook.
  
Os elementos de dados nesse fluxo são armazenados em ordem de byte little-endian, imediatamente após uns aos outros na seguinte ordem especificada:
  
- **FieldDefinitionCount**: DWORD (4 bytes), o número de definições de campo neste fluxo. Esta é a contagem de elementos na **matriz FieldDefinitions.**
    
- **FieldDefinitions**: uma matriz de estruturas de fluxo FolderFieldDefinitionW. A contagem dessa matriz é igual ao elemento de dados **FieldDefinitionCount.**
    
A **matriz FieldDefinitions** deve ser "terminada em nulo" tendo seu último campo Common.FieldType do elemento FolderFieldDefinitionW igual a ftNull.
  
## <a name="folderfielddefinitiona-stream-structure"></a>Estrutura de fluxo FolderFieldDefinitionA

Uma estrutura de fluxo FolderFieldDefinitionA contém uma definição de um campo definido pelo usuário com o nome do campo armazenado em ANSI.
  
Os elementos de dados nesse fluxo são armazenados em ordem de byte little-endian, imediatamente após uns aos outros na seguinte ordem especificada:
  
- **FieldType**: FldType (4 bytes), o tipo deste campo.
    
- **FieldNameLength**: WORD (2 bytes), o número de elementos na **matriz FieldName.**
    
- **FieldName**: uma matriz de CHAR. Esta é a representação de página de CP_ACP ANSI do nome do campo. A contagem dessa matriz é igual a **FieldNameLength**. O nome do campo deve satisfazer as restrições no parâmetro Name, conforme especificado no [Método UserProperties.Add.](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) 
    
   > [!NOTE]
   > Por motivos de compatibilidade herdada, o Outlook pode ser capaz de lidar com alguns valores **FieldName** que não satisfazem essas restrições, mas esses casos não são cobertos por este tópico. 
  
- **Common**: uma estrutura de fluxo FolderFieldDefinitionCommon.
    
## <a name="folderfielddefinitionw-stream-structure"></a>Estrutura de Fluxo de FolderFieldDefinitionW

Uma estrutura de fluxo FolderFieldDefinitionW contém uma definição de um campo definido pelo usuário com o nome do campo armazenado em Unicode.
  
Os elementos de dados nesse fluxo são armazenados em ordem de byte little-endian, imediatamente após uns aos outros na seguinte ordem especificada:
  
- **FieldType**: FldType (4 bytes), o tipo deste campo.
    
- **FieldNameLength**: WORD (2 bytes), o número de elementos na **matriz FieldName.**
    
- **FieldName**: uma matriz de WCHAR. Esta é a representação Unicode (UTF-16) do nome do campo. A contagem dessa matriz é igual a **FieldNameLength**. O nome do campo deve satisfazer as restrições no parâmetro Name, conforme especificado no [Método UserProperties.Add.](https://msdn.microsoft.com/library/microsoft.office.interop.outlook.userproperties.add.aspx) 
    
   > [!NOTE]
   > Por motivos de compatibilidade herdada, o Outlook pode ser capaz de lidar com alguns valores **FieldName** que não satisfazem essas restrições, mas esses casos não são cobertos por este tópico. 
  
- **Common**: uma estrutura de fluxo FolderFieldDefinitionCommon.
    
## <a name="fldtype-enumeration"></a>Enumeração FldType

Os valores de enumeração **FldType** estão listados na tabela a seguir. 
  
|Nome|Valor|Significado|
|:-----|:-----|:-----|
|ftNull  <br/> |0x0  <br/> |Esse tipo de campo é usado para encerrar uma matriz de definições de campo nulo.  <br/> |
|ftString  <br/> |0x1  <br/> |Texto  <br/> |
|ftInteger  <br/> |0x3  <br/> |Inteiro  <br/> |
|ftTime  <br/> |0x5  <br/> |Data/Hora  <br/> |
|ftBoolean  <br/> |0x6  <br/> |Sim/Não  <br/> |
|ftDuration  <br/> |0x7  <br/> |Duration  <br/> |
|ftMultiString  <br/> |0xB  <br/> |Palavras-chave  <br/> |
|ftFloat  <br/> |0xC  <br/> |Número ou Porcentagem  <br/> |
|ftCurrency  <br/> |0xE  <br/> |Moeda  <br/> |
|ftCalc  <br/> |0x12  <br/> |Fórmula  <br/> |
|ftSwitch  <br/> |0x13  <br/> |Combinação de tipo mostrando apenas o primeiro campo não vazio, ignorando os subsequentes.  <br/> |
|ftConcat  <br/> |0x17  <br/> |Combinação de tipos de campos de junção e fragmentos de texto entre si.  <br/> |
   
## <a name="folderfielddefinitioncommon-stream-structure"></a>Estrutura de fluxo FolderFieldDefinitionCommon

A FolderFieldDefinitionCommon stream structure contains the data of a user-defined field definition that is common to both a FolderFieldDefinitionA and a FolderFieldDefinitionW.
  
Os elementos de dados nesse fluxo são armazenados em ordem de byte little-endian, imediatamente após uns aos outros na seguinte ordem especificada:
  
- **PropSetGuid**: GUID (16 bytes), o GUID do conjunto de propriedades do nome da propriedade MAPI correspondente do campo da pasta. O valor desse campo deve ser igual a PS_PUBLIC_STRINGS, a menos que o tipo de campo seja **ftNone.** Nesse caso, o valor desse campo deve ser igual a GUID_NULL. 
    
   > [!NOTE]
   > Por motivos de compatibilidade herdada, o Outlook pode ser capaz de lidar com alguns valores **PropSetGuid** que não satisfazem essa restrição, no entanto, esses casos não são cobertos por este tópico. 
  
- **fcapm**: DWORD (4 bytes), uma combinação de zero ou mais sinalizadores dos valores dos quais e significados estão listados na tabela a seguir. Sinalizadores com o mesmo valor têm significados dependentes do tipo do campo, ou seja, valor FldType.
    
    |Nome do sinalizador|Valor|Significado|
    |:-----|:-----|:-----|
    |FCAPM_CAN_EDIT  <br/> |0x00000001  <br/> |O campo é editável.  <br/> |
    |FCAPM_CAN_SORT  <br/> |0x00000002  <br/> |O campo é sortível.  <br/> |
    |FCAPM_CAN_GROUP  <br/> |0x00000004  <br/> |O campo é agrupado.  <br/> |
    |FCAPM_MULTILINE_TEXT  <br/> |0x00000100  <br/> |O campo pode conter várias linhas de texto.  <br/> |
    |FCAPM_PERCENT  <br/> |0x01000000  <br/> |Esse campo do tipo ftFloat é um campo de porcentagem.  <br/> |
    |FCAPM_DATEONLY  <br/> |0x01000000  <br/> |Esse campo do tipo ftTime é um campo de hora somente data.  <br/> |
    |FCAPM_UNITLESS  <br/> |0x01000000  <br/> |Para esse campo do tipo ftInteger, nenhuma unidade é permitida no formato de exibição; por exemplo, formatos como "Computador - 640 K..." não são permitidas.  <br/> |
    |FCAPM_CAN_EDIT_IN_ITEM  <br/> |0x80000000  <br/> |O campo pode ser editado no item: especificamente para formulários personalizados.  <br/> |
   
- **dwString**: DWORD (4 bytes). Consulte a primeira observação a seguir.
    
- **dwBitmap**: DWORD (4 bytes). Consulte a primeira observação a seguir.
    
- **dwDisplay**: DWORD (4 bytes). Consulte a primeira observação a seguir.
    
- **iFmt**: INT (4 bytes). Para os tipos de campo que têm a caixa de combinação "Format:" nas caixas de diálogo "Novo Campo", "Editar Campo" e "Propriedades do Campo", o índice baseado em 0 do formato selecionado nessa caixa de combinação. Para os tipos de campo sem essa caixa de combinação, deve ser 0. O valor do campo junto com o tipo de campo determina exclusivamente os valores dos campos **dwString**, **dwBitmap** e **dwDisplay,** consulte a primeira observação a seguir.
    
- **wszFormulaLength**: WORD (2 bytes), o número de elementos na **matriz wszFormulaLength.**
    
- **wszFormulaLength**: uma matriz de WCHAR. Esta é a representação Unicode (UTF-16) da cadeia de caracteres de fórmula do campo em seu formato padrão. Consulte a segunda observação a seguir para ver a descrição dos formatos padrão e de interface do usuário da fórmula de um campo. A contagem dessa matriz é igual a **wszFormulaLength**. A cadeia de caracteres de fórmula deve ser uma cadeia de caracteres vazia, a menos que o tipo de campo seja **ftCalc**, **ftSwitch** ou **ftConcat**.
    
> [!NOTE]
> Embora os valores **de dwString**, **dwBitmap** e **dwDisplay** sejam determinados exclusivamente com base no valor **FldType** e no valor **iFmt,** que são redundantes, seus valores corretos ainda são necessários para o processamento correto da definição de campo pelo Outlook. Não há uma descrição simples do algoritmo que executa essa determinação. 
> 
> Portanto, para descobrir quais valores **dwString**, **dwBitmap** e **dwDisplay** correspondem a um determinado valor **FldType** e **valor iFmt,** realize um teste criando um campo definido pelo usuário desse tipo e com esse formato selecionado na caixa de combinação **Format,** supondo sua aplicabilidade, inspecione o fluxo **FolderUserFields** resultante que o Outlook cria para esse campo definido pelo usuário. 
  
A fórmula do campo em seu formato de interface do usuário é editada  na caixa de texto Fórmula das caixas de diálogo Novo Campo **,** Editar Campo e Propriedades do Campo para o campo definido pelo usuário.  O algoritmo para converter uma fórmula do formato de interface do usuário para o formato padrão depende do tipo de campo conforme descrito no seguinte: 
- Para campos de tipos **ftCalc** e **ftSwitch**, o formato padrão para campos integrados, que propriedades MAPI correspondentes não são propriedades nomeadas do tipo MNID STRING, é obtido substituindo fragmentos de nome de campo, ou seja, por fragmentos \_ `[<field_name>]` `[_<field_dispid_decimal>]` . 

  Por exemplo, se o formato da interface do usuário de uma fórmula para um campo do tipo Formula **,** que é **ftCalc**, com o idioma da interface do usuário do Office sendo inglês dos EUA, é , onde está o nome de um campo definido pelo `[Business Phone] & [My custom field]` usuário, o formato padrão dessa fórmula seria `My custom field` `[_14856] & [My custom field]` .

- Para campos do tipo **ftConcat**, o formato padrão é obtido executando o seguinte:

  1. Truncar espaço em branco à frente e à frente. 
  2. Analisar a fórmula em uma sequência de fragmentos dos dois tipos a seguir: 
     - Um nome de campo entre colchetes, ou seja, `[<field_name>]` . 
     - Uma substring que não contém colchetes.   
      Garanta que nenhum fragmento do segundo tipo seja adjacente na sequência. Se a fórmula não puder ser analisada dessa forma, ela será considerada inválida. 
  3. Execute a mesma substituição para fragmentos do primeiro tipo dos **campos ftCalc** e **ftSwitch.** 
  4. Para cada fragmento do segundo tipo, escape todos os caracteres de aspas duplas ("""), se algum, com dois caracteres de aspas duplas consecutivas, e coloque-o entre aspas duplas. 
  5. Insere uma cadeia de caracteres e comercial ( `&` ) entre cada par de fragmentos adjacentes.
 
  Por exemplo, usando o idioma inglês dos EUA da interface do usuário do Office, se o formato da interface do usuário de uma fórmula para um campo do tipo **ftConcat** for , onde está o nome de um campo definido pelo usuário, o formato padrão para tal fórmula seria `text1 [Business Phone] "text2" [My custom field]` `My custom field` `""text1" & [_14856] & """text2""" & [My custom field]"` . 
  
## <a name="see-also"></a>Confira também

- [Exemplo de fluxo de FolderUserFields](folderuserfields-stream-sample.md)
- [Adicionar uma definição para um novo User-Defined campo](how-to-add-a-definition-for-a-new-user-defined-field.md)

