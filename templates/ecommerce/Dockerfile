FROM node:20-alpine
RUN npm install -g pnpm
WORKDIR /app
COPY . .
RUN sed -i 's/"workspace:\*"/"\*"/g' package.json
RUN pnpm install --no-frozen-lockfile
RUN pnpm build
EXPOSE 3000
CMD ["pnpm", "start"]
