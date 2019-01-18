---
title: Propriedade Bookmark (ADO)
TOCTitle: Bookmark property (ADO)
ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15)
ms:contentKeyID: 48543287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 17818fe2b4f826cbcfbbb3955817c2b5d99ab6a3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704767"
---
# <a name="bookmark-property-ado"></a>Propriedade Bookmark (ADO)


**Aplica-se a**: Access 2013, o Office 2013

Aponta um indicador que identifica com exclusividade o registro atual em um objeto [Recordset](recordset-object-ado.md) ou define o registro atual em um objeto **Recordset** para o registro identificado por um indicador válido.

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Configura ou retorna uma expressão **Variant** que avalia um indicador válido.

## <a name="remarks"></a>Comentários

Use a propriedade **Bookmark** para salvar a posição do registro atual e retornar para esse registro a qualquer momento. Bookmarks estão disponíveis apenas em objetos **Recordset** que ofereçam suporte à funcionalidade de indicadores.

Quando um objeto **Recordset** é aberto, cada um dos registros tem um indicador exclusivo. Para salvar o indicador do registro atual, atribua o valor da propriedade **Bookmark** a uma variável. Para retornar rapidamente àquele registro depois de se mover para um registro diferente, defina a propriedade **Bookmark** do objeto **Recordset** com o valor daquela variável.

Talvez o usuário não seja capaz de exibir o valor do indicador. Além disso, os usuários não devem esperar que os indicadores sejam comparados diretamente  dois indicadores referentes ao mesmo registro podem ter valores diferentes.

Se você usar o método [Clone](clone-method-ado.md) para criar uma cópia de um objeto **Recordset**, as definições da propriedade **Bookmark** para os objetos **Recordset** original e duplicado serão idênticas e você poderá usá-las alternadamente. Contudo, não é possível usar indicadores de objetos **Recordset** diferentes alternadamente, mesmo que eles tenham sido criados a partir da mesma fonte ou comando.

**Uso de serviço de dados remotos** Quando usado em um objeto **Recordset** do lado do cliente, a propriedade **Bookmark** está sempre disponível.

