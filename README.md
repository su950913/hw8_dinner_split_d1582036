[hw8_dinner_split_d1582036.ipynb](https://github.com/user-attachments/files/34735136/hw8_dinner_split_d1582036.ipynb)
# hw8_dinner_split_d1582036{
  "cells": [
    {
      "cell_type": "code",
      "source": [
        "# 1. 原始資料：保留文字資料，另外建立整理後的變數。\n",
        "event_name = \"  WEEKEND DINNER  \"\n",
        "meal_amount = \" NT$1,200 \"\n",
        "people = \"4\"\n",
        "\n",
        "service_rate = 0.10\n",
        "discount = 100\n",
        "budget_per_person = 300\n",
        "\n",
        "# 2. 整理聚餐名稱。\n",
        "clean_event_name = event_name.strip().lower()\n",
        "\n",
        "# 3. 清理餐費文字，再轉換餐費與人數的型別。\n",
        "clean_meal_text = meal_amount.replace(\"NT$\", \"\").replace(\",\", \"\").replace(\" \", \"\")\n",
        "meal_value = float(clean_meal_text)\n",
        "people_count = int(people)\n",
        "\n",
        "# 4. 先按原始餐費計算服務費，再扣除折價券。\n",
        "service_fee = meal_value * service_rate\n",
        "total_amount = meal_value + service_fee - discount\n",
        "amount_per_person = total_amount / people_count\n",
        "\n",
        "# 5. 比較結果直接保存為 bool。等於預算時不算超過。\n",
        "is_over_budget = amount_per_person > budget_per_person\n",
        "\n",
        "# 6. 輸出時才將金額格式化為兩位小數。\n",
        "print(f\"聚餐名稱：{clean_event_name}\")\n",
        "print(f\"原始餐費：{meal_value:.2f} 元\")\n",
        "print(f\"服務費：{service_fee:.2f} 元\")\n",
        "print(f\"折價券：{discount:.2f} 元\")\n",
        "print(f\"應付總額：{total_amount:.2f} 元\")\n",
        "print(f\"分攤人數：{people_count} 人\")\n",
        "print(f\"每人費用：{amount_per_person:.2f} 元\")\n",
        "print(f\"每人預算：{budget_per_person:.2f} 元\")\n",
        "print(f\"是否超過預算：{is_over_budget}\")"
      ],
      "metadata": {
        "id": "gLje2dnXpAVl",
        "outputId": "718c0cd2-ae62-41e9-8c5d-9262dc7c07ea",
        "colab": {
          "base_uri": "https://localhost:8080/"
        }
      },
      "execution_count": 11,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "聚餐名稱：weekend dinner\n",
            "原始餐費：1200.00 元\n",
            "服務費：120.00 元\n",
            "折價券：100.00 元\n",
            "應付總額：1220.00 元\n",
            "分攤人數：4 人\n",
            "每人費用：305.00 元\n",
            "每人預算：300.00 元\n",
            "是否超過預算：True\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# 1. 原始資料：保留文字資料，另外建立整理後的變數。\n",
        "event_name = \"  WEEKEND DINNER  \"\n",
        "meal_amount = \" NT$1,200 \"\n",
        "people = \"5\"\n",
        "\n",
        "service_rate = 0.10\n",
        "discount = 100\n",
        "budget_per_person = 300\n",
        "\n",
        "# 2. 整理聚餐名稱。\n",
        "clean_event_name = event_name.strip().lower()\n",
        "\n",
        "# 3. 清理餐費文字，再轉換餐費與人數的型別。\n",
        "clean_meal_text = meal_amount.replace(\"NT$\", \"\").replace(\",\", \"\").replace(\" \", \"\")\n",
        "meal_value = float(clean_meal_text)\n",
        "people_count = int(people)\n",
        "\n",
        "# 4. 先按原始餐費計算服務費，再扣除折價券。\n",
        "service_fee = meal_value * service_rate\n",
        "total_amount = meal_value + service_fee - discount\n",
        "amount_per_person = total_amount / people_count\n",
        "\n",
        "# 5. 比較結果直接保存為 bool。等於預算時不算超過。\n",
        "is_over_budget = amount_per_person > budget_per_person\n",
        "\n",
        "# 6. 輸出時才將金額格式化為兩位小數。\n",
        "print(f\"聚餐名稱：{clean_event_name}\")\n",
        "print(f\"原始餐費：{meal_value:.2f} 元\")\n",
        "print(f\"服務費：{service_fee:.2f} 元\")\n",
        "print(f\"折價券：{discount:.2f} 元\")\n",
        "print(f\"應付總額：{total_amount:.2f} 元\")\n",
        "print(f\"分攤人數：{people_count} 人\")\n",
        "print(f\"每人費用：{amount_per_person:.2f} 元\")\n",
        "print(f\"每人預算：{budget_per_person:.2f} 元\")\n",
        "print(f\"是否超過預算：{is_over_budget}\")"
      ],
      "metadata": {
        "id": "Xptq606PpKEl",
        "outputId": "efc7e067-a3f5-4ec3-b9c9-9953490de4e8",
        "colab": {
          "base_uri": "https://localhost:8080/"
        }
      },
      "execution_count": 12,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "聚餐名稱：weekend dinner\n",
            "原始餐費：1200.00 元\n",
            "服務費：120.00 元\n",
            "折價券：100.00 元\n",
            "應付總額：1220.00 元\n",
            "分攤人數：5 人\n",
            "每人費用：244.00 元\n",
            "每人預算：300.00 元\n",
            "是否超過預算：False\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# 1. 原始資料：保留文字資料，另外建立整理後的變數。\n",
        "event_name = \"  WEEKEND DINNER  \"\n",
        "meal_amount = \" NT$1,200 \"\n",
        "people = \"4\"\n",
        "\n",
        "service_rate = 0.10\n",
        "discount = 220\n",
        "budget_per_person = 300\n",
        "\n",
        "# 2. 整理聚餐名稱。\n",
        "clean_event_name = event_name.strip().lower()\n",
        "\n",
        "# 3. 清理餐費文字，再轉換餐費與人數的型別。\n",
        "clean_meal_text = meal_amount.replace(\"NT$\", \"\").replace(\",\", \"\").replace(\" \", \"\")\n",
        "meal_value = float(clean_meal_text)\n",
        "people_count = int(people)\n",
        "\n",
        "# 4. 先按原始餐費計算服務費，再扣除折價券。\n",
        "service_fee = meal_value * service_rate\n",
        "total_amount = meal_value + service_fee - discount\n",
        "amount_per_person = total_amount / people_count\n",
        "\n",
        "# 5. 比較結果直接保存為 bool。等於預算時不算超過。\n",
        "is_over_budget = amount_per_person > budget_per_person\n",
        "\n",
        "# 6. 輸出時才將金額格式化為兩位小數。\n",
        "print(f\"聚餐名稱：{clean_event_name}\")\n",
        "print(f\"原始餐費：{meal_value:.2f} 元\")\n",
        "print(f\"服務費：{service_fee:.2f} 元\")\n",
        "print(f\"折價券：{discount:.2f} 元\")\n",
        "print(f\"應付總額：{total_amount:.2f} 元\")\n",
        "print(f\"分攤人數：{people_count} 人\")\n",
        "print(f\"每人費用：{amount_per_person:.2f} 元\")\n",
        "print(f\"每人預算：{budget_per_person:.2f} 元\")\n",
        "print(f\"是否超過預算：{is_over_budget}\")"
      ],
      "metadata": {
        "id": "3Ml1ZONNpZEs",
        "outputId": "1358bda1-8439-4fa4-82b6-5f813bba5621",
        "colab": {
          "base_uri": "https://localhost:8080/"
        }
      },
      "execution_count": 14,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "聚餐名稱：weekend dinner\n",
            "原始餐費：1200.00 元\n",
            "服務費：120.00 元\n",
            "折價券：220.00 元\n",
            "應付總額：1100.00 元\n",
            "分攤人數：4 人\n",
            "每人費用：275.00 元\n",
            "每人預算：300.00 元\n",
            "是否超過預算：False\n"
          ]
        }
      ]
    }
  ],
  "metadata": {
    "colab": {
      "name": "歡迎使用 Colab",
      "provenance": []
    },
    "kernelspec": {
      "display_name": "Python 3",
      "name": "python3"
    }
  },
  "nbformat": 4,
  "nbformat_minor": 0
}
