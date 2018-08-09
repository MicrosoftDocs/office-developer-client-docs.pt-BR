---
title: Elemento de DataRecordSet (DataRecordSets_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Armazena, formata, atualiza e expõe os dados consultados de um banco de dados no Microsoft Visio.
ms.openlocfilehash: 157213476214c736367b724dd6ca944060c53467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771662"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a>Elemento de DataRecordSet (DataRecordSets_Type complexType) ('Visio XML')

Armazena, formata, atualiza e expõe os dados consultados de um banco de dados no Microsoft Visio.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |Recordsets.XML  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Contém todos os elementos de **DataRecordset** no documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Contém o XML que está em conformidade com o esquema XML clássico do ADO para um recordset do ADO e que descreve os dados no conjunto de registros de dados.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Define uma regra que compara uma coluna no elemento pai **DataRecordset** com um item de dados da forma da última bem-sucedida automática vinculação ação executada na interface do usuário.  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Define como uma coluna de dados aparece na janela **Dados externos** na interface do usuário do Visio e qualifica os dados na coluna definindo seu tipo de dados e formatação.  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contém todos os elementos de **DataColumn** em um conjunto de registros de dados.  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Identifica um ou mais colunas de chave primária no conjunto de registros de dados.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Indica uma linha no conjunto de registros de dados vinculada a uma forma que está em conflito após a atualização dos registros de dados.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Mapeia uma linha do conjunto de registros de dados a uma forma.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Attribute**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Soma de verificação  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Um valor de soma de verificação, geradas pelo Visio e com base nas propriedades do conjunto de registros de dados. Defina este attirbute como 0; O Visio recalcula esse valor em tempo de execução.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Command  <br/> |XSD: String  <br/> |opcional  <br/> |A cadeia de caracteres de comando usada para dados de consulta da fonte de dados.  <br/> |Valores do tipo xsd: String.  <br/> |
|Conexão  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |A identificação de conexão para o objeto **DataConnection** associado. Não existe para fontes de dados XML.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |obrigatório  <br/> |A identificação de recordset dados, exclusiva dentro do documento.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Nome  <br/> |XSD: String  <br/> |opcional  <br/> |A exibição (ou "amigável") nome do conjunto de registros de dados.  <br/> |Valores do tipo xsd: String.  <br/> |
|NextRowID  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |O próximo disponíveis Visio identificação da linha.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Options  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Opções que se aplicam ao conjunto de registros de dados. Os valores possíveis podem ser qualquer combinação de um ou mais daqueles mostrados na tabela a seguir.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|RefreshInterval  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Frequência (em minutos) Visio atualiza automaticamente o conjunto de registros de dados. Este valor deve ser 1 ou maior.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|RefreshNoReconciliationUI  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Se a interface do usuário reconciliação de dados deve ser desabilitada. True (1) para desativar a interface de usuário (UI). False (0) para habilitar a interface do usuário.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|RefreshOverwriteAll  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Se deseja substituir alterações do usuário a itens de dados da forma em formas vinculadas aos dados quando o conjunto de registros de dados for atualizado.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|ReplaceLinks  <br/> |XSD:unsignedInt  <br/> |opcional  <br/> |Define como os vínculos forma-dados são tratados quando as formas são copiadas ou recortadas. 1 para substituir os vínculos existentes na forma de destino. 0 para manter os vínculos existentes na forma de destino.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|RowOrder  <br/> |XSD:Boolean  <br/> |opcional  <br/> |Se usar a ordem das linhas no conjunto de registros de dados como a chave primária. True (1) se a linha IDs são determinados pelo ordem da linha. False (0) se a linha IDs são determinados pelos valores das colunas de chave primária de registros de dados.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|TimeRefreshed  <br/> |XSD: DateTime  <br/> |opcional  <br/> |A data e hora que o conjunto de registros de dados foi atualizado pela última vez.  <br/> |Valores do tipo xsd: DateTime.  <br/> |
   

