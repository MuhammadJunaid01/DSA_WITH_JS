লিনিয়ার সার্চ কমন একটি সার্চিং এলগরিদম, জাভাস্ক্রিপ্টের বিল্টিইন মেথড indexOf(), includes(), find(), and findIndex(),এসব বিল্টইন মেথড জাভাস্ক্রিপ্টের বিহাইন্ড দ্যা সীনে লিনিয়ার সার্চ ব্যবহার করে আমাদেরকে আমাদের কাঙ্কিত রেজাল্ট দিয়ে থাকে।

এটি সবচেয়ে সবচেয়ে সহজ এলগরিদম, লিনিয়ার সার্চ একটি এ্যারে এর প্রতিটি এলিমেন্ট এর উপর লুপ চালায়, যখন টার্গেটকে খুঁজে পাই তখন লুপ বন্ধ বন্ধ হয়ে যায় এবং আমাদেরকে সাধারণত টার্গেট কত নাম্বার এলিমেন্টে খুঁজে পেয়েছে তার ইনডেক্স রিটার্ন করে।

চলেন এবার লিনিয়ার সার্চ কোডে ইমপ্লিমেন্ট করে দেখি—

COPY
const linearSearch = (arr, target) => {
for (let i = 0; i < arr.length; i++) {
if (arr[i] === target) {
return i;
}
}
return -1;
};
console.log(linearSearch([1, 2, 3, 4, 5, 78, 99, 111, 400, 7, 300, 20], 7)); //return index 9
লুপ এর ভিতরে আমার ইফ কন্ডিশন দিয়ে প্রত্যেকটি এলিমেন্টকে চেক করতেছি টার্গেট এর সাথে ম্যাচ করছে কি না,if কন্ডিশন সত্য হলে আমরা ইফ এর ভিতর থেকে আইকে (এখানে আই অ্যাারে এর এলিমেন্ট এর পজিশন নাম্বার হিসেবে গণ্য হবে ) রিটার্ন করে দিচ্ছি, ইফ কন্ডিশন যতক্ষণ সত্য হবেনা ততক্ষণ প্রতেকটি অ্যাারে এর এলিমেন্ট এর উপর লুপ চলতে থাকবে, যদি অ্যারে এর মধ্যে টার্গেট খুঁজে না পাই, তখন লুপ এর বাহির থেকে আমরা -1 রিটার্ন করতেছি।

এখানে একটা বিষয় ক্লিয়ার করে বুঝে নেয়া উচিত, আমরা কেনো if পরে এলস কন্ডিশন বসিয়ে else এর ভিতর থেকে -1 রিটার্ন করলাম না ??? এর কারন হলো যখন প্রথমবার if কন্ডিশন মিথ্যা হবে তখন else এর ভিতর থেকে যদি রিটার্ন করে দিই ,তখন লুপ বন্ধ হয়ে যাবে এবং বাকি এলিমেন্ট আর চেক করবে না, এই জন্য আমরা লুপ এর বাহিরে গিয়ে -1 রিটার্ন করেছি,যাতে করে অ্যাারে এর প্রত্যেকটি এলিমেন্ট চেক করে, if কন্ডিশন যদি সত্য না হয় তখন লুপ শেষ হওয়ার পর লুপ বাহিরে গিয়ে -1 রিটার্ন করে দিয়েছি।

ধন্যবাদ, আজকের মত এখানেই শেষ, সবাই ভালো থাকবেন।
