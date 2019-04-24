---
title: Ação de macro SetField (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 9ae292b0-fde0-4c2b-ba23-23e90365597d
description: A ação DefinirCampo pode ser usada para atribuir um valor a um campo.
ms.openlocfilehash: c67c66c238b68512aec90cf6d82d7d497e16ecf1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307893"
---
# <a name="setfield-macro-action-access-custom-web-app"></a>Ação de macro SetField (aplicativo Web personalizado do Access)

A ação **DefinirCampo** pode ser usada para atribuir um valor a um campo. 
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
> [!NOTE]
> A ação **DefinirCampo** está disponível somente em Macros de Dados. 
  
## <a name="setting"></a>Configuração

A ação **DefinirCampo** tem os seguintes listados na tabela a seguir. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
|**Nome** <br/> |Uma cadeia de caracteres que identifica o campo.  <br/> |
|**Valor** <br/> |Uma expressão que especifica o valor a ser atribuído ao campo.  <br/> |
   
## <a name="remarks"></a>Comentários

A ação **SetField** não pode ser usada fora de um bloco de dados **[CriarRegistro](createrecord-data-block-access-custom-web-app.md)** ou **[editarregistro](editrecord-data-block-access-custom-web-app.md)** . 
  

