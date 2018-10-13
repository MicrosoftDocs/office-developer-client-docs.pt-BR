---
title: Elemento ConjuntoDeRegistrosDeDados (DataRecordSets_Type tipo complexo) 'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Armazena, formata, atualiza e expõe dados consultados de um banco de dados no Microsoft Visio.
ms.openlocfilehash: e2baaeed38318f35d4bd4ce4269f71b6304b148f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387283"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a>Elemento ConjuntoDeRegistrosDeDados (DataRecordSets_Type tipo complexo) 'Visio XML (')

Armazena, formata, atualiza e expõe dados consultados de um banco de dados no Microsoft Visio.
  
## <a name="element-information"></a>Elemento de informações

|||
|:-----|:-----|
|**Tipo de elemento** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Arquivo de esquema** <br/> |VisioSchema15.xsd  <br/> |
|**Partes do documento** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Definição

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elementos e atributos

Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, consulte a seção de definição. 
  
### <a name="parent-elements"></a>Elementos pai

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Contém todos os elementos **DataRecordset** do documento.  <br/> |
   
### <a name="child-elements"></a>Elementos filho

|**Elemento**|**Tipo**|**Descrição**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Contém o XML que está em conformidade com o clássico esquema XML ADO de um conjunto de registros ADO e que descreve os dados no conjunto de registros de dados XML.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Define uma regra que compara uma coluna pai do elemento **ConjuntoDeRegistrosDeDados** com um item de dados de forma na última ação de vinculação automática bem-sucedida, executadas na interface do usuário.  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Define a aparência de uma coluna de dados na janela **Dados Externos** na interface de usuário do Visio e qualifica os dados na coluna definindo o tipo de dados e formatação.  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Contém todos os elementos de **DataColumn** em um conjunto de registros de dados.  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Identifica uma ou mais colunas de chave primárias do conjunto de dados.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Indica uma linha do conjunto de dados vinculados a uma forma que está em conflito após a atualização de conjunto do registros de dados.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Mapas de uma linha de conjunto de registros de dados para uma forma.  <br/> |
   
### <a name="attributes"></a>Atributos

|**Atributo**|**Tipo**|**Obrigatório**|**Descrição**|**Valores possíveis**|
|:-----|:-----|:-----|:-----|:-----|
|Soma de verificação  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Um valor de soma de verificação, gerado pelo Visio, e com base em propriedades do conjunto de registros de dados. Definir este atributo como 0; O Visio recalculará esse valor no tempo de execução.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Comando  <br/> |xsd:string  <br/> |opcional  <br/> |A cadeia de caracteres de comando usada para dados de consulta da fonte de dados.  <br/> |Valores do tipo xsd:string.  <br/> |
|ConnectionID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |A ID de conexão para o objeto **conexão de dados** associado. Não existem para fontes de dados XML.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |obrigatório  <br/> |A ID de conjunto de registros dados, exclusiva no documento.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Nome  <br/> |xsd:string  <br/> |opcional  <br/> |A exibição (ou nome) amigável do conjunto de registros de dados.  <br/> |Valores do tipo xsd:string.  <br/> |
|NextRowID  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |A próxima ID de linha disponível Visio.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|Opções  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Opções para aplicar ao conjunto de registros de dados. Os valores possíveis podem ser qualquer combinação de um ou mais valores mostrados na tabela a seguir.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|RefreshInterval  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |A frequência (em minutos) que o Visio atualiza automaticamente o conjunto de registros de dados. Esse valor deve ser definido como 1 ou maior.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|RefreshNoReconciliationUI  <br/> |xsd:boolean  <br/> |opcional  <br/> |Caso a interface de reconciliação dados do usuário deva ser desabilitada. Verdadeiro (1) para desabilitar a interface do usuário (IU). FALSO (0) para habilitar a interface do usuário (IU).  <br/> |Valores do tipo xsd:boolean.  <br/> |
|RefreshOverwriteAll  <br/> |xsd:boolean  <br/> |opcional  <br/> |Caso substitua mudanças do usuário para moldar itens de dados nos formatos ligados aos dados, quando o registro de dados for atualizado.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|ReplaceLinks  <br/> |xsd:unsignedInt  <br/> |opcional  <br/> |Define como os links de dados de forma são tratados quando as formas são copiadas ou recortadas. 1 para substituir os links existentes na forma de destino. 0 para manter os links existentes na forma de destino.  <br/> |Valores do tipo xsd:unsignedInt.  <br/> |
|RowOrder  <br/> |xsd:boolean  <br/> |opcional  <br/> |Caso use a ordem das linhas do conjunto de dados como chave primária. Verdadeiro (1), se as IDs de linha forem determinadas pela ordem da linha. FALSO (0) se as IDs de linha forem determinadas pelos valores em colunas de chave primárias do conjunto de registros de dados.  <br/> |Valores do tipo xsd:boolean.  <br/> |
|TimeRefreshed  <br/> |xsd:dateTime  <br/> |opcional  <br/> |A data e a hora em que o conjunto de registros de dados foi atualizado pela última vez.  <br/> |Valores do tipo xsd:dateTime.  <br/> |
   

