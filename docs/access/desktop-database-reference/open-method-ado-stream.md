---
title: Método Open (Stream do ADO)
TOCTitle: Open method (ADO Stream)
ms:assetid: fa2e6aaa-e9f5-009c-f3a0-050a00abf9b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250275(v=office.15)
ms:contentKeyID: 48548833
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a943209ce329d59fb4846ed18fd008bc45803da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288382"
---
# <a name="open-method-ado-stream"></a>Método Open (Stream do ADO)


**Aplica-se ao:** Access 2013, Office 2013


Abre um objeto [Stream](stream-object-ado.md) para manipular fluxos de dados de texto ou binários.

## <a name="syntax"></a>Sintaxe

*Stream*. Open *Source*, *Mode*, *OpenOptions*, *UserName*, *Password*

## <a name="parameters"></a>Parâmetros

|Parâmetro|Descrição|
|:--------|:----------|
|*Source* |Opcional. Um valor **Variant** que especifica a fonte dos dados para o **Stream**. *Source* may contain an absolute URL string that points to an existing node in a well-known tree structure, like an email or file system. Uma URL deve ser especificada usando a palavra-chave URL ("URL=*esquema*://*pasta do* / *servidor*"). De forma alternativa, *Source* pode conter uma referência para um objeto [Record](record-object-ado.md) já aberto, que abre o fluxo padrão associado ao **Record**. Se *Source* não for especificado, um **Stream** será instanciado e aberto, não associado a fonte base alguma por padrão. Para obter mais informações sobre esquemas de URL e seus provedores associados, consulte [URLs absolutas e relativas.](absolute-and-relative-urls.md)|
|*Mode* |Opcional. Um valor [ConnectModeEnum](connectmodeenum.md) que especifica o modo de acesso para o **Stream** resultante (por exemplo, leitura/gravação ou somente leitura). O valor padrão é **adModeUnknown**. Consulte a propriedade [Mode](mode-property-ado.md) para obter mais informações sobre modos de acesso. Se *Mode* não for especificado, ele será herdado do objeto de origem. Por exemplo, se o **Record** de origem for aberto no modo somente leitura, o **Stream** também será aberto no modo somente leitura por padrão.|
|*OpenOptions* |Opcional. Um valor [StreamOpenOptionsEnum](streamopenoptionsenum.md). O valor padrão é **adOpenStreamUnspecified**.|
|*UserName* |Opcional. Um valor **String** que contém a identificação do usuário que, se necessária, acessa o objeto **Stream**.|
|*Password* |Opcional. Um valor **String** que contém a senha que, se necessária, acessa o objeto **Stream**.|

## <a name="remarks"></a>Comentários

Quando um objeto **Record** é passado como o parâmetro de origem, os parâmetros *UserID* e *Password* não são utilizados porque o acesso ao objeto **Record** já está disponível. Da mesma forma, o [Mode](mode-property-ado.md) do objeto **Record** é transferido para o objeto **Stream**. Quando *Source* não é especificado, o **Stream** aberto não contém dados e tem [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) igual a zero (0). To Para evitar a perda de quaisquer dados gravados nesse **Stream** quando o **Stream** for fechado, salve o **Stream** com os métodos [CopyTo](copyto-method-ado.md) ou [SaveToFile](savetofile-method-ado.md) ou salve-o em outro local da memória.

Um valor **adOpenStreamFromRecord** de *OpenOptions* identifica o conteúdo do parâmetro *Source* para ser um objeto **Record** já aberto. O comportamento padrão é tratar *Source* como uma URL que aponta diretamente para um nó em uma estrutura em árvore, tal como um arquivo. O fluxo padrão associado a esse nó será aberto.

Enquanto o **Stream** não estiver aberto, será possível ler todas as propriedades somente leitura do **Stream**. Se um **Stream** for aberto assincronamente, todas as operações subsequentes (que não sejam a verificação de [State](state-property-ado.md) e outras propriedades somente leitura) serão bloqueadas até que a operação **Open** seja concluída.

Além das opções discutidas acima, por meio da não especificação de *Source* é possível simplesmente instanciar um objeto **Stream** em memória sem associá-lo a uma fonte base. Você pode adicionar dados dinamicamente ao fluxo simplesmente pela gravação de dados de texto ou binários no **Stream** com [Write](write-method-ado.md) ou [WriteText](writetext-method-ado.md), ou pelo carregamento de dados a partir de um arquivo com [LoadFromFile](loadfromfile-method-ado.md).

