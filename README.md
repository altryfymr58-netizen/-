import { AbsoluteFill, useCurrentFrame, interpolate } from "remotion";

export const MyAd = () => {
  const frame = useCurrentFrame();

  const opacity = interpolate(frame, [0, 15], [0, 1]);

  return (
    <AbsoluteFill
      style={{
        backgroundColor: "white",
        justifyContent: "center",
        alignItems: "center",
        fontFamily: "Arial",
        color: "#222",
      }}
    >
      <h1 style={{ fontSize: 60, opacity }}>📘 الأحياء صار أسهل معنا!</h1>

      <p style={{ fontSize: 40, marginTop: 20 }}>
        شرح + ملخصات + اختبارات تفاعلية
      </p>

      <p style={{ fontSize: 35, marginTop: 40 }}>
        ✅ الاختبار الشهري: <s>150</s> → <b style={{ color: "green" }}>120</b>
      </p>
      <p style={{ fontSize: 35 }}>
        ✅ الاختبار النهائي: <s>150</s> → <b style={{ color: "green" }}>120</b>
      </p>
      <p style={{ fontSize: 35 }}>
        🌟 الباقة الشاملة: <s>300</s> →{" "}
        <b style={{ color: "green" }}>210</b>
      </p>

      <h2 style={{ marginTop: 60, color: "blue" }}>
        🎯 احجز باقتك الآن!
      </h2>
    </AbsoluteFill>
  );
};
