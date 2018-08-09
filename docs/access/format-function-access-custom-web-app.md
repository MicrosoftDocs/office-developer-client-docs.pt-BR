---
title: Função Format (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Retorna um valor formatado de acordo com um padrão especificado.
ms.openlocfilehash: 974b56ab8e6bc3f97c1931ba67ca9cd08c3511c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765091"
---
# <a name="format-function-access-custom-web-app"></a>Função Format (aplicativo Web personalizado do Access)

Retorna um valor formatado de acordo com um padrão especificado.
  
> [!NOTE]
> O recurso de armazenamento de nuvem descrito neste artigo não é mais suportado no Office 2013 e Office 2016 e pode resultar no seguinte erro: > *Sorry, vamos ter problemas no servidor, portanto não podemos adicionar \<service\> conveniente. Tente novamente mais tarde.* > Para armazenamento em nuvem para o Office Online, o Office para iOS e do Office para Android, você pode pesquisar em nosso [Programa de parceria de armazenamento de nuvem do Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxe

 **Formato** (*Expressão*, *formato*) 
  
A função **Format** contém os seguintes argumentos. 
  
|**Nome do argumento**|**Descrição**|
|:-----|:-----|
| *Expressão*  <br/> |Expressão de um tipo de dados com suporte para formatar.  <br/> |
| *Format*  <br/> | Um formato padrão. O argumento format deve conter uma cadeia de caracteres de formato válido, como uma cadeia de caracteres de formato padrão (por exemplo, "C" ou "D"), ou como um padrão de caracteres personalizados para datas e os valores numéricos (por exemplo, "MMMM dd, yyyy (dddd)"). Para obter mais informações, consulte comentários.  <br/> |
   
## <a name="remarks"></a>Comentários

Para o parâmetro *Format* , você pode passar cadeias de caracteres que correspondam a qualquer um dos seguintes padrões: 
  
- [Cadeias de caracteres de formato numérico padrão](http://msdn.microsoft.com/en-us/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [Cadeias de caracteres de formato numérico personalizado](http://msdn.microsoft.com/en-us/library/0c899ak8%28v=vs.110%29.aspx)
    
- [As cadeias de caracteres de formato padrão de data e hora](http://msdn.microsoft.com/en-us/library/az4se3k1%28v=vs.110%29.aspx)
    
- [As cadeias de caracteres de formato de data e hora personalizado](http://msdn.microsoft.com/en-us/library/8kb3ddd4%28v=vs.110%29.aspx)
    
Você não pode usar a função **Format** nas seguintes áreas do Access 2013 web apps: 
  
- Colunas calculadas no nível de tabela
    
- Macros de interface do usuário
    
- Expressões em modos de exibição (por exemplo, em formulários)
    

