---
title: Método Save-ActiveX Data Objects (ADO)
TOCTitle: Save method (ADO)
ms:assetid: 02dab13b-f947-b96d-46ea-0def3ed8f28f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248793(v=office.15)
ms:contentKeyID: 48542968
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0a3762c3d4fdb8cc833259b0435b225690d677ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308915"
---
# <a name="save-method-ado"></a>Método Save (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Salva o [Recordset](recordset-object-ado.md) em um arquivo ou objeto [Stream](stream-object-ado.md).

## <a name="syntax"></a>Sintaxe

*Recordset*. Salvar*destino*, *PersistFormat*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Destination* |Opcional. Uma **Variant** que representa o nome de caminho completo do arquivo em que o **Recordset** deve ser salvo, ou uma referência a um objeto **Stream**.|
|*PersistFormat* |Opcional. Um valor [PersistFormatEnum](persistformatenum.md) que especifica o formato no qual o **Recordset** deve ser salvo (XML ou ADTG). O valor padrão é **adPersistADTG**.|

## <a name="remarks"></a>Comentários

O método **Save** pode ser chamado apenas em um **Recordset** aberto. Utilize o método [Open](open-method-ado-recordset.md) para posteriormente restaurar o **Recordset** do *Destination*.

Se a propriedade [Filter](filter-property-ado.md) estiver em efeito para o **Recordset**, apenas as linhas acessíveis sob o filtro serão salvas. Se o **Recordset** for hierárquico, o **Recordset** filho atual e seus filhos serão salvos, incluindo o **Recordset** pai. Se o método **Save** de um **Recordset** filho for chamado, o filho e seus filhos serão salvos, mas o pai não o será.

Na primeira vez que você salva o **Recordset**, é opcional especificar *Destination*. Se você omitir *Destination*, será criado um novo arquivo com o nome definido como o valor da propriedade [Source](source-property-ado-recordset.md) do **Recordset**.

Omita *Destination* ao chamar **Save** subsequentemente após o primeiro salvamento, ou ocorrerá um erro em tempo de execução. Se você chamar **Save** subsequentemente com um novo *Destination*, o **Recordset** será salvo no novo destino. No entanto, o novo destino e o destino original estarão ambos abertos.

**Save** não fecha o **Recordset** ou o *Destination*, de forma que é possível continuar a trabalhar com o **Recordset** e salvar as alterações mais recentes. *Destination* permanece aberto até que o **Recordset** seja fechado.

Por motivos de segurança, o método **Save** permite apenas a utilização de definições de segurança baixas e personalizadas a partir de um script executado pelo Microsoft Internet Explorer. Para obter uma explicação mais detalhada dos problemas de segurança, consulte "ADO and RDS Security Issues in Microsoft Internet Explorer" sob Artigos Técnicos do ActiveX Data Objects (ADO) nos Artigos Técnicos de Acesso a Dados da Microsoft.

Se o método **Save** for chamado enquanto uma operação de busca, execução ou atualização assíncrona de **Recordset** estiver em andamento, **Save** aguardará até que a operação assíncrona seja concluída.

Os registros são salvos a partir da primeira linha do **Recordset**. Quando o método **Save** for concluído, a posição de linha atual será movida para a primeira linha do **Recordset**.

Para obter melhores resultados, defina a propriedade [CursorLocation](cursorlocation-property-ado.md) para **adUseClient** com **Save**. Se o provedor não oferecer suporte a toda a funcionalidade necessária para salvar objetos **Recordset**, o Cursor Service fornecerá essa funcionalidade.

Quando um **Recordset** for persistido com a propriedade **CursorLocation** definida como **adUseServer**, a capacidade de atualização do **Recordset** será limitada. Normalmente, apenas atualizações, inserções e exclusões de tabela única são permitidas (dependendo da funcionalidade do provedor). O método [Resync](resync-method-ado.md) também está indisponível nessa configuração.

> [!NOTE]
> [!OBSERVAçãO] O salvamento de um **Recordset** com **Fields** do tipo **adVariant**, **adIDispatch** ou **adIUnknown** não é suportado pelo ADO e pode causar resultados imprevisíveis.

Somente **filtros** na forma de cadeias de caracteres de critérios ( \> por exemplo, DataDoPedido ' 12/31/1999 ') afetam o conteúdo de um **Recordset**persistente. Os filtros criados com uma Matriz de **Bookmarks** ou utilizado um valor de **FilterGroupEnum** não afetarão o conteúdo do **Recordset** persistido. Essas regras são aplicadas a **Recordsets** criados com cursores do cliente ou do servidor.

Como o parâmetro *Destination* pode aceitar qualquer objeto que suporte a interface IStream do banco de dados OLE, é possível salvar um **Recordset** diretamente no objeto de Resposta do ASP. Para obter mais detalhes, consulte o [Cenário de Persistência de Recordset XML](xml-recordset-persistence-scenario.md).

Também e possível salvar um **Recordset** em formato XML para uma instância de um objeto MSXML DOM, conforme mostrado no seguinte código Visual Basic:

> [!NOTE]
> [!OBSERVAçãO] Duas limitações são aplicadas ao salvar **Recordsets** hierárquicos (formas de dados) em formato XML. Não é possível salvar em XML se o **Recordset** hierárquico contiver atualizações pendentes e não é possível salvar um **Recordset** hierárquico parametrizado.

Um Recordset salvo em formato XML é salvo utilizando-se o formato UTF-8. Quando um arquivo desse tipo for carregado em um Stream do ADO, o objeto Stream não tentará abrir um Recordset a partir do fluxo a menos que a propriedade Charset do fluxo esteja definida para o valor apropriado do formato UTF-8.

