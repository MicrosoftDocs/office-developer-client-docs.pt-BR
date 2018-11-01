---
title: Propriedade ActualSize (ADO)
TOCTitle: ActualSize property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 10/16/2018
mtps_version: v=office.15
ms.openlocfilehash: 627f4fe93340c69b62f81c1b10ebf231938eea89
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873179"
---
# <a name="actualsize-property-ado"></a>Propriedade ActualSize (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Indica o tamanho real do valor de um campo.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Retorna um valor **Long**. Alguns provedores talvez permitam que essa propriedade seja definida para reservar espaço para dados BLOB, caso em que o valor padrão é 0.

## <a name="remarks"></a>Comentários

Use a propriedade **ActualSize** para retornar o tamanho real do valor de um objeto [Field](field-object-ado.md). Para todos os campos, a propriedade **ActualSize** é somente leitura. Se o ADO não puder determinar o tamanho do valor do objeto **Field**, a propriedade **ActualSize** retornará **adUnknown**.

As propriedades **ActualSize** e [DefinedSize](definedsize-property-ado.md) são diferentes. Um objeto **Field** com um tipo declarado de **adVarChar** e um comprimento máximo de 50 caracteres retornará um valor de propriedade **DefinedSize** de 50, mas o valor da propriedade **ActualSize** a ser retornado será o tamanho dos dados armazenados no campo para o registro atual. **Fields** com um **DefinedSize** maior do que 255 bytes serão tratados como colunas de comprimento variável.

